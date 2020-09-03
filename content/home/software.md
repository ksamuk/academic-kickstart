+++
# A Projects section created with the Portfolio widget.
widget = "featured"  # See https://sourcethemes.com/academic/docs/page-builder/
headless = true  # This file represents a page section.
active = true  # Activate this widget? true/false
weight = 70  # Order that this section will appear.

title = "Software"
subtitle = ""

[content]
  # Page type to display. E.g. project.
  page_type = "project"
  
  # Filter toolbar (optional).
  # Add or remove as many filters (`[[content.filter_button]]` instances) as you like.
  # To show all items, set `tag` to "*".
  # To filter by a specific tag, set `tag` to an existing tag name.
  # To remove toolbar, delete/comment all instances of `[[content.filter_button]]` below.
  
  # Default filter index (e.g. 0 corresponds to the first `[[filter_button]]` instance below).
  filter_default = 0
  
  # [[content.filter_button]]
  #   name = "All"
  #   tag = "*"
  
  # [[content.filter_button]]
  #   name = "Deep Learning"
  #   tag = "Deep Learning"
  
  # [[content.filter_button]]
  #   name = "Other"
  #   tag = "Demo"

[design]
  # Choose how many columns the section has. Valid values: 1 or 2.
  columns = "2"

  # Toggle between the various page layout types.
  #   1 = List
  #   2 = Compact
  #   3 = Card
  #   5 = Showcase
  view = 1

  # For Showcase view, flip alternate rows?
  flip_alt_rows = false

[design.background]
  # Apply a background color, gradient, or image.
  #   Uncomment (by removing `#`) an option to apply it.
  #   Choose a light or dark text color by setting `text_color_light`.
  #   Any HTML color name or Hex value is valid.
  
  # Background color.
  # color = "navy"
  
  # Background gradient.
  # gradient_start = "DeepSkyBlue"
  # gradient_end = "SkyBlue"
  
  # Background image.
  # image = "background.jpg"  # Name of image in `static/img/`.
  # image_darken = 0.6  # Darken the image? Range 0-1 where 0 is transparent and 1 is opaque.

  # Text color (true=light or false=dark).
  # text_color_light = true  
  
[advanced]
 # Custom CSS. 
 css_style = ""
 
 # CSS class.
 css_class = ""
+++

# *syntR* 
<img src="https://raw.githubusercontent.com/ksamuk/syntR/master/inst/figures/logo.png", width="120", height="135", align="right">
**Reproducible identification of chromosomal rearrangements**


Co-developed with [Dr. Kate Ostevik](https://www.kateostevik.com/), *syntR* is an R package for the reproducible identification of synteny blocks and chromosomal rearrangments via comparison of two genetic maps. syntR implements an error-aware clustering algorithm specifically designed for the highly linear structure of comparative genetic map data. syntR can be used to identify synteny blocks using any type of ordered genetic markers.

Read more about *syntR* here: https://ksamuk.github.io/syntR/

# *pixy* 
<img src="https://raw.githubusercontent.com/ksamuk/pixy/master/docs/pixy_logo.png", width="120", height="135", align="right">
**Unbiased estimation of nucleotide diversity and divergence with missing data**


Co-developed with [Dr. Katharine Korunes](https://katharinekorunes.weebly.com/), *pixy* is a command-line tool for painlessly and correctly estimating average nucleotide diversity within (π) and between (d<sub>xy</sub>) populations from a VCF. In particular, pixy facilitates these calculations using VCFs containing invariant sites, missing sites, and missing genotypes.

Read more about *pixy* here: https://github.com/ksamuk/pixy

