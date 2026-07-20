---
layout: page
title: Opportunities
permalink: /team/opportunities/
---

There are many ways to contribute to our mission of reducing existential risk from artificial intelligence.

## Open roles

We are building a team of exceptional researchers and staff.

{% assign open_jobs = site.jobs | sort: "title" %}
{% for job in open_jobs %}
**[{{ job.title }}]({{ job.url | relative_url }})** — {{ job.job.location_display }} · {{ job.job.salary_display }} / {{ job.job.salary_period | default: "year" }}
{% endfor %}

## Research Partnerships

**[Principles of Intelligence Fellowship](https://princint.ai/programs/fellowship/)** - We collaborate with this program to mentor interdisciplinary researchers transitioning into AI safety.

If your organization is interested in a research partnership, please [reach out](/team/community/).

## Support Our Work

As a non-profit research organization, we rely on philanthropic support to fund our research and operations.

If you are considering support, please see [Research Overview](/research/) and [Publications](/research/publications/) for our public-facing overview and contributions so far.

If you are interested in supporting us financially, please [contact us](/team/community/).
