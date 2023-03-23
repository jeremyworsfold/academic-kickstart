---
# A Recent Blog Posts section created with the Pages widget.
# This section displays recent blog posts from `content/post/`.

widget : slider  # See https://sourcethemes.com/academic/docs/page-builder/
headless : true  # This file represents a page section.
weight : 80  # Order that this section will appear.
draft : true

# ... Put Your Section Options Here (section position etc.) ...

# Slide interval.
# Use `false` to disable animation or enter a time in ms, e.g. `5000` (5s).
interval: 3000

# Minimum slide height.
# Specify a height to ensure a consistent height for each slide.
#height: 600px

design:
  is_fullscreen: true
  loop: true

item:

  - title: "Postgraduate Student Seminars"
    content: 'Cycle through to see the recent talk titles or click below to see a list of all from this year.'
    align: left
    #overlay_color: '#00bbff'
    cta_label: PSS talks
    cta_url: 'pss/'
    cta_icon_pack: fas
    cta_icon: graduation-cap
    background:
        position: center
        #color: '#333'
        brightness: 0.5
        media: featured.png
        fit: cover

  - title: "AIMS: **An overview of moving mesh methods**"
    content: "Seb Scott 18/02/2020"
    align: left
    overlay_color: '#00bbff'
    cta_label: More information here
    cta_url: 'https://wiki.bath.ac.uk/display/cnmseminar/2019-20+Schedule'
    cta_icon_pack: fas
    cta_icon: graduation-cap


  - title: "An overview of moving mesh methods"
    content: 'Simone Appella, 12/02/2021'
    align: left
    overlay_color: '#00bbff'
    cta_label: Abstract
    cta_url: 'pss/simone/'
    cta_icon_pack: fas
    cta_icon: graduation-cap

  - title: "TBC"
    content: 'Allen Hart 04/03/2021'
    align: left
    overlay_color: '#00bbff'
    cta_label: Abstract
    cta_url: 'pss/allen/'
    cta_icon_pack: fas
    cta_icon: graduation-cap


---