Black in AI
============

 Based on this theme: [Demo](http://t413.com/SinglePaged) and  [github project page](https://github.com/t413/SinglePaged)

## Setup & Basics

This site uses [jekyll](https://jekyllrb.com/), to get started, clone or fork, and see the [jekyll quickstart guide](https://jekyllrb.com/docs/quickstart/)

Content can all be edited in markdown files in `_segments/` or `_speakers`

To edit style, change the CSS in `_includes/css`

The main page is the `index.html` will guide to most structure and `_config.yml` defines many site variables. 

## Adding a section on main page:
 - Add md file to `_segments` folder, date for order (oldest at top)
 - include yaml front matter as below
 
```yaml
---  
title: will display in the menu  
bg: background color, 
color: text color  
emph: color of headings  
style: [justify or center, as defined in css]
---
```

__Note:__ colors can be defined using standard html names or using plain english names as defined in `_config.yaml` 


## Speakers
Speakers are also a [collection](https://jekyllrb.com/docs/collections/), to add: 
 - create a markdown file named after the speaker
 - add yaml front matter as below
 - name image same as the md file up to extension add it to `img/` directory
 - the `layout: speaker` line should be included as is, that tells jekyll how to process the `.md` file for inclusion elsewhere
 - see `2000-01-05-program.md` on how to include speakers within another section
 - all speakers are added to `/speaker-list ` page

```yaml
---
layout: speaker   
display: Name as to be displayed on page  
img: image name with extenstion (that must be in img dir)  
type: [keynote, dinner]
link: url to the person's site
---
```

Speakers can be added to another part of the site using:
```
{% assign sp = site.speakers | where:"display", "Ciira Maina" | first %}
{{sp.output}}
```
The output is controlled by `_layouts/speaker.html`.

The speakers are also output to a `/speaker-list.html`. 
