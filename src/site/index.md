---
title: Google Sheets data feed example. With Eleventy.
layout: default
---


## Content from an external data source

The lists below showing NBA AllStar starting fives for 2019 were sourced from [a Google Sheet](https://docs.google.com/spreadsheets/d/1CfI6XGm9OjjNKGr3kXRSKVLui_gkHZdadoOPIiNgE9s/edit#gid=0) as [JSON](https://spreadsheets.google.com/feeds/list/1CfI6XGm9OjjNKGr3kXRSKVLui_gkHZdadoOPIiNgE9s/od6/public/values?alt=json) at site build time.


### Eastern Conference All Stars
<ul class="listing">
{%- for item in sheet.East -%}
  <li>{{ item.name }} - {{ item.team }}</li>
{%- endfor -%}
</ul>

### Western Conference All Stars
<ul class="listing">
{%- for item in sheet.West -%}
  <li>{{ item.name }} - {{ item.team }}</li>
{%- endfor -%}
</ul>




## About this example

This site is an example of using [Eleventy's JavaScript Data Files](https://www.11ty.io/docs/data-js/) which simplify pulling content from remote data sources and making them available as  objects to be used globally across an Eleventy site.

- This page is pulling content from a read-only [Google Sheets feed](https://spreadsheets.google.com/feeds/list/1CfI6XGm9OjjNKGr3kXRSKVLui_gkHZdadoOPIiNgE9s/od6/public/values?alt=json).
- The [code is available to inspect on GitHub]({{ pkg.repository.url}}) and more information is available from the [ReadMe]({{ pkg.repository.url}}/blob/master/README.md).
- You can also clone [the repo]({{ pkg.repository.url}}) and deploy your own version of the site to [Netlify](https://www.netlify.com) for free all in a couple of clicks by hitting the button below. That one down there. 👇


## Clone and deploy!

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/philhawksworth/example-read-from-sheets)



