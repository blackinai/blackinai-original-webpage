Black in AI
============

 Based on this theme: [Demo](http://t413.com/SinglePaged) and  [github project page](https://github.com/t413/SinglePaged)


## Adding a section on main page:
 - Add md file to `_posts` folder, date for order (oldest at top)
 - include yaml front matter
 
```yaml
---  
title: will display in the menu  
bg: background color, 
color: text color  
emph: color of headings  
---
```

__Note:__ colors can be defined using standard html names or using plain english names as defined in `_config.yaml` 


## Speakers are a collection, to add: 
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
---
```