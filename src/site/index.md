---
title: Eleventy Example - Google Sheets data feed
layout: default
---


## Content from an external data source

The list below was sourced from [a Google Sheet](https://docs.google.com/spreadsheets/d/1CfI6XGm9OjjNKGr3kXRSKVLui_gkHZdadoOPIiNgE9s/edit#gid=0) as JSON at site build time.

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

This site is an example of using [Eleventy's JavaScript Data Files](https://www.11ty.io/docs/data-js/) which simplify pulling content from remote data sources and making them available as  objects to be used globally across and Eleventy site.

- This page is pulling content from a read-only Google Sheets feed.
- The code is available to inspect on GitHub and more information is available from the ReadMe.
- You can also clone the repo and deploy your own version of the site to Netlify for free all in a couple of clicks by hitting the button below 👇


## Clone and deploy!

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/philhawksworth/example-read-from-sheets)



