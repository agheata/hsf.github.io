---
title: Summary of GSoC 2021 Projects and Supervisors
layout: plain
year: 2021
---

## Full List of Proposals

Please check later, project proposals will be added until Feb 15, 2021

{:.table .table-hover .table-striped}
{% assign sorted_proposals = site.gsocproposals | sort: 'title' %}
{% for proposal in sorted_proposals %}{% capture u_proposal_org %}{{ organization | upcase }}{% endcapture %}
{%- assign strings = proposal.url | split: '/' -%}
{%- assign proposal_year = strings[2] | plus: 0 -%}
{%- if proposal_year == page.year %}
| [ {{ proposal.title }} ]( {{ proposal.url }} ) |
{%- endif -%}
{% endfor %}