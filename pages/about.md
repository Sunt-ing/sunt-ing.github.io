---
layout: page
title: About Me
description: Sunt
keywords: Sun Ting, 孙挺, Sunt
comments: true
menu: About Me
permalink: /about/


subtitle:   <h2>Download My CV</h2>
          
            <a role="button" class="btn btn-primary hvr-grow-shadow" href="/assets/files/CV_Ting_Sun_EN.pdf" target="_blanks">
                <span class="flag-icon flag-icon-gb"></span> English
            </a>

                            
css: ['about.css', 'sidebar-popular-repo.css', '../../bower_components/flag-icon-css/css/flag-icon.min.css']
---

Hello, I am Sun Ting (孙挺), an undergraduate in the computer science department of SUSTech (Southern University of Science and Technology).

## Contact

{% for website in site.data.social %}
* {{ website.sitename }}：[@{{ website.name }}]({{ website.url }})
{% endfor %}

## Skill Keywords

{% for category in site.data.skills %}
### {{ category.name }}
<div class="btn-inline">
{% for keyword in category.keywords %}
<button class="btn btn-outline" type="button">{{ keyword }}</button>
{% endfor %}
</div>
{% endfor %}

