---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "How to use Python for scientific research"
subtitle: "Maintaining a personal Python package for scientific research"
summary: ""
authors: [admin]
tags: [Scientific Computing]
categories: [Scientific Computing]
date: 2020-12-14T21:44:52Z
lastmod: 2020-12-14T21:44:52Z
featured: false
draft: true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: "Smart"
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

The world seems to be split into two types of projects. The ones maintained by software engineers committed to maintaining usability, robustness and efficiency of a package. Then there are those entitiled `simulation-2_old.py` with cut and pasted code from previous versions which has only been looked at by one person. It might seem ovbious which is the better project but the word *better* here is important. 

The context of what the code is for is crucial. If all was needed was a short simulation to demonstrate some result then perhaps the second type is a more efficient use of time. The importance of changeability and speed of implementation is an important factor in scientific research. 

This article tries to present to you a way of balancing these two extremes. There are always more things you can add to a project and this is what I have found works for me but my opinion may also change on what it necessary. 

## General things we want our project to do ##

No matter the language you're working in I believe these core ideas are things we want to embody in our project. The main point of them is to give yourself a consistent structure to adapt code and test out new things while maintaining a system and making sure someone else could use it.

- **Save data**: Saving the results of simulations or processing data is incredibly important. It can be tempting to just make some changes and see what happens but then find out those results would have been useful to revisit and either it takes a while to run them again or you can't remember the parameters you chose. Saving data in an easily understandable format can lots of time in the long run. 
- **Separation between visualising results and the simulations or preprocessing**: This point follows on from the previous one because if we save our data from the early stages of our workflow then we should be able to load it in an produce all the plots we need from that data. We've all been there when you realise you labelled your axes incorrectly on a plot of some results which took a couple of hours to run and you don't have the raw data available any more. I'll give more details on why this might be useful later.
- **Good Documentation**: Writing documentation such that a layperson could understand you code is definitely too much to ask and is not relevant but it should be good enough that a person familiar with the programming language and the field or research would be able to follow what you have done and why.
- **Distribution**: If your work eventually gets published it would be great if a reader could look at your code and run it for themselves so that they can gain the same level of trust in your code as they have for whatever mathematical proofs you have in the text.


## Why Python? ##


{{< chart data="annealing" >}}

Before saying anything else in this section I will acknowledge that ultimately this comes down to personal preference. Each person develops their own style of working and habits or have a specific field of research which lend themselves to particular languages. Before deciding which language to use, consider things such as:
- Support for the things you would like to do: Are there packages associated with the things you want to code in a certain language which will make your life easier?
- Do you know the language already?: Rarely much use in starting from scratch with a language if it's a small project unless you are particularly interested in learning a new language.

With that out the way, here is my biased case for why python is good for small research projects. The typical cyclical argument for python is that lots of people use so you should use it too. There is a huge community of people using it so chances are there will be applicable, well-maintained packages out there to help you do the things you want.

It's incredibly flexible so if the scope of your project changes it's relatively easy to adapt your code or just extend it to add new features. Since this is a small project it's nice to not have to worry about what is sometimes called *boiler plate code* which can plague lower level languages. Lower level languages often insist you specify the types of your variables or defines destructors to your classes or how data is copied between classes. All of this often allows the code to run faster and ensures it does exactly what you want but slows down your start when all you really want to do is see if your idea works initially.

Python is rarely the most efficient or fastest language to use out of the box compared with things like MATLAB or R if you use them correctly. However, there is always scope for increasing the efficiency of your code in Python down the line. Initally this can just be making sure you have optimised your code with vectorisation through using numpy. Going deeper you can use things such as the Multiprocessing or MPI4py modules for parallel computing or you could convert the core aspects of your code to Cython or pure C code which can greatly increase the speed of your code. The details of how to do this and the benefits of it might be the subject of a blog another time.

## How to Structure your Python project ##
This is how I've chosen to layout my projects, it follows the standard for python packages but has some tweaks for using as a personal project which may not be considered best practice but is relatively easy to use.
```
exampleproject
│   README.md
│   setup.py
│
├───data
├───docs
│       optional-documentation.md
├───exampleproject
│   │   __init__.py
│   │
│   ├───environment
│   │       base.py
│   │       derived.py
│   │       __init__.py
│   │
│   └───otherfiles
│           utils.py
│           __init__.py
│
├───notebooks
│       01-feature1.ipynb
│       02-feature2.ipynb
│
└───scripts
        feature1.py
```

## Documentation and Commenting ##


## Presenting your findings ##

I find as well that a significant amount of the experimentation happens in the plotting of the raw data. Given some underlying simulation I might want to try out all sorts of different plots and so having the raw data saved allows me to quickly try out visualising a variety of features. Having said this, it can be useful to visualise one or two things while you are producing your data to give you confidence it is all behaving as it should.

number them so there's some structure but maybe not necessary

load in results, can then just plot it and convert it to some other format to be plotted professionally like pgfplots.