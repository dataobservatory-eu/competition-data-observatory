---
# An instance of the Portfolio widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: portfolio

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 20

title: Services
subtitle: 'Automated Data Services'

content:
  # Page type to display. E.g. project.
  page_type: services

  # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
  filter_default: 0

  # Filter toolbar (optional).
  # Add or remove as many filters (`filter_button` instances) as you like.
  # To show all items, set `tag` to "*".
  # To filter by a specific tag, set `tag` to an existing tag name.
  # To remove the toolbar, delete the entire `filter_button` block.
  filter_button:
  - name: All
    tag: '*'
  - name: Open Data
    tag: Open Data
  - name: Documentation & Codebooks
    tag: metadata
  - name: Data API
    tag: open-data, 
  - name: Reproducible Research
    tag: reproducible

design:
  # Choose how many columns the section has. Valid values: '1' or '2'.
  columns: '2'

  # Toggle between the various page layout types.
  #   1 = List
  #   2 = Compact
  #   3 = Card
  #   5 = Showcase
  view: 5

  # For Showcase view, flip alternate rows?
  flip_alt_rows: false
---


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td style="text-align: center;">{{< figure src="/media/img/gems/edgar-soto-gb0BZGae1Nk-unsplash.jpg" caption="[What’s the Problem with Open Data?](/data/open-gov/#open-data-problems)" numbered="false" >}}</td>
<td style="text-align: center;">{{< figure src="/media/img/gems/Diamond_Polisher.jpg" caption="[How We Add Value?](/data/open-gov/#open-data-value-added)" numbered="false" >}}</td>
<td style="text-align: center;">{{< figure src="/media/img/plots/gems/Uncut-diamond_Edit.jpg" caption="[Is There Value in It?](/data/open-gov/#is-there-value-left-in-open-data) </br>If it’s money on the street, why nobody’s picking it up?" numbered="false" >}}</td>
<td style="text-align: center;">{{< figure src="/media/img/gems/Udachnaya_pipe.jpg" caption="[Datasets Should Work Together to Give Information](/data/open-gov/#data-integration)</br>Data is only potential information, raw and unprocessed." numbered="false" >}}</td>
</tr>
</tbody>
</table>

