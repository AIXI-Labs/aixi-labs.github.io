---
layout: page
title: Opportunities
breadcrumb:
  - title: Team
    url: /team/
permalink: /team/opportunities/
---

There are many ways to contribute to our mission of reducing existential risk via understanding intelligence from first principles. For most people, the best way to get involved will be via the educational resources and reading group on our [Learning & Community page](/team/community/). Many of our research fellows began as regular contributors to the reading group.

## Open roles

We are building a team of exceptional researchers and staff. Click on the toggles below to learn more.

{% assign open_jobs = site.jobs | sort: "title" %}
{% comment %}
  Each role expands in place (click the arrow or title) to show its full description.
  The standalone posting pages in _jobs/ still build: they carry the Google for Jobs data.
{% endcomment %}
{% for job in open_jobs %}
<details class="toggle-section" markdown="0">
  <summary>
    <h3 class="toggle-section-title">{{ job.title }}</h3>
    <p class="toggle-section-meta">{{ job.job.location_display }} · {{ job.job.salary_display }} / {{ job.job.salary_period | default: "year" }}</p>
  </summary>
  <div class="toggle-section-body">
    {{ job.content }}
    <p class="job-apply"><a href="{{ job.job.apply_url }}" class="job-apply-button" target="_blank" rel="noopener">Apply now</a></p>
  </div>
</details>
{% endfor %}

## Research Partnerships

**[Principles of Intelligence Fellowship](https://princint.ai/programs/fellowship/)** - We collaborate with this program to mentor interdisciplinary researchers transitioning into AI safety.

<hr class="section-sep" />

{% include link-buttons.html
   left_text="If your organization is interested in a research partnership:"
   left_label="Contact Us" left_url="/contact/" %}
