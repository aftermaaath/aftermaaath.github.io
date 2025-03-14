---
# Mr. Green Jekyll Theme (https://github.com/MrGreensWorkshop/MrGreen-JekyllTheme)
# Copyright (c) 2022 Mr. Green's Workshop https://www.MrGreensWorkshop.com
# Licensed under MIT

layout: default
# Notes page
---
{%- include multi_lng/get-lng-by-url.liquid -%}
{%- assign lng = get_lng -%}

{%- assign notes_data = page.page_data | default: site.data.content.notes[lng].page_data -%}

<div class="multipurpose-container links-heading-container">
  <h1>{{ notes_data.main.header | default: "Notes" }}</h1>
  <p>{{ notes_data.main.info | default: "No data, check page_data in [language]/tabs/notes.md front matter or _data/content/links/[language].yml" }}</p>
  <div class="multipurpose-button-wrapper">
    {%- for category in notes_data.category %}
      <a href="#{{ category.type }}" role="button" class="multipurpose-button link-buttons" style="background-color:{{ category.color }};">{{ category.title }}</a>
    {% endfor -%}
  </div>
</div>

{%- if site.data.conf.others.notes.use_rows_as_link -%}{%- assign hover_class = "table-hover" -%}{%- endif -%}
{%- for category in notes_data.category %}
<div class="multipurpose-container link-container" id="{{ category.type }}" style="border-left-color:{{ category.color }};">
  <h2>{{ category.title }}</h2>
  <table class="table {{ hover_class }}">
    <thead>
      <tr>
        <th>{{ site.data.lang[lng].links.link_text }}</th>
        <th>{{ site.data.lang[lng].links.info_text }}</th>
      </tr>
    </thead>
    <tbody>
      {%- for list in notes_data.list %}
        {%- if list.type != category.type %}{% continue %}{% endif -%}
        {%- if site.data.conf.others.links.use_rows_as_link -%}
          {%- capture link_onclick -%} onclick="window.open('{{ list.url }}', '_self');" style="cursor: pointer;" {%- endcapture -%}
          {%- capture link_url -%} <b>{{ list.title }}</b> {%- endcapture -%}
        {% else %}
          {%- assign link_onclick = nil -%}
          {%- capture link_url -%} <a href="{{ list.url }}" rel="noopener noreferrer"><b>{{ list.title }}</b></a> {%- endcapture -%}
        {%- endif %}
        <tr class="link-item" {{ link_onclick }}>
          <td>
            <p>{{ link_url }}</p>
          </td>
          <td>
            <p>{{ list.info }}</p>
          </td>
        </tr>
      {%- endfor %}
    </tbody>
  </table>
</div>
{% endfor %}
