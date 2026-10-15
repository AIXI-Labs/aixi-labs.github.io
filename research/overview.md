---
layout: page
title: Overview
breadcrumb:
  - title: Research
    url: /research/
permalink: /research/
---

<img src="{{ '/assets/img/aixi_formula.png' | relative_url }}" alt="AIXI formula" class="research-formula" />

## What's in a name?

AIXI is the leading mathematical model of artificial superintelligence, representing the **maximum theoretical limit of AI capabilities.**

Alongside the [name's many previous meanings](https://www.hutter1.net/ai/uaibook.htm#meaning), AIXI now also stands for the AI X-risk Initiative. Though, we usually just call ourselves AIXI Labs.

## What do we do?

<p class="summary-hint" hidden>Click the toggle below to switch between the compact and ‘plain English’ summaries.</p>

<div class="summary-toggle">
  <button type="button" class="summary-switch" role="switch" aria-checked="false"
          aria-controls="summary-compact summary-plain" aria-label="Plain English summary" hidden>
    <span class="summary-switch-knob"></span>
  </button>
  <div class="summary-text">
    <div id="summary-compact">
      <p>We model AI risk factors and safety mitigations in terms of AIXI variants, and develop the means to translate them to real AI agents. This enables rigorous testing of both the risk factors and the safety mitigations.</p>
    </div>
    <div id="summary-plain" hidden>
      <p>AIXI is a mathematical model of an ideal, general-purpose AI agent. It can’t be built in practice. But because it’s defined precisely, we can reason about it rigorously.</p>
      <p>We create variants of AIXI that include specific risks or safety measures. This lets us test:</p>
      <ul>
        <li>The risks AI could pose</li>
        <li>Specific ways of reducing those risks</li>
      </ul>
      <p>We also develop methods to apply our findings to real-world AI systems.</p>
    </div>
  </div>
</div>

<script>
  // Toggle between the compact and plain-English summaries. Without JS the
  // compact text shows and the switch and hint stay hidden.
  (function () {
    var button = document.querySelector('.summary-switch');
    var compact = document.getElementById('summary-compact');
    var plain = document.getElementById('summary-plain');
    button.hidden = false;
    document.querySelector('.summary-hint').hidden = false;
    button.addEventListener('click', function () {
      var on = button.getAttribute('aria-checked') !== 'true';
      button.setAttribute('aria-checked', String(on));
      compact.hidden = on;
      plain.hidden = !on;
    });
  })();
</script>

## Why this approach?

Most AI research today sits in one of two categories:

- Methods that are fast and mathematically clean in narrow settings
- Methods that are practical for frontier applications but opaque to safety analysis.

Our core focus is the third intersection: methods that are **general** enough to describe powerful agents and amenable to mathematical **analysis** to support rigorous safety claims.

Aligning a hypothetical superintelligence requires a concerted effort in this historically neglected direction.

<img class="approach-diagram" src="{{ '/assets/img/aixi_venn_diagram_v4.svg' | relative_url }}" alt="Venn diagram of Fast, General and Analyzable methods: Frontier AI is Fast and General, Textbook RL is Fast and Analyzable, and AIXI, our focus, is General and Analyzable" />

Thus, we formally examine behaviors, capabilities, risks and mitigations for idealized agents in fully general environments. We aim to port the most promising methods to modern LLM-based agents, and test principled hypotheses on these agents. Since our analyses are based on a very general model of superintelligence, we gain confidence that any experimentally validated conclusions will generalize and scale to future AI systems.

<hr class="section-sep" />

<div class="focus-cards">
  <section class="focus-card">
    <h3>Basic Science</h3>
    <p>How do AI agents work? How do they (mis)generalize? What are their incentives?</p>
  </section>
  <section class="focus-card">
    <h3>Risk Factors</h3>
    <p>Would AI agents scheme to deceive or take power? Under what conditions? Can we reliably test for this?</p>
  </section>
  <section class="focus-card">
    <h3>Safety Mitigations</h3>
    <p>Do existing safety proposals generalize in the limit of high capabilities? Does modeling this limit suggest any new safety techniques?</p>
  </section>
</div>

<hr class="section-sep" />

{% include link-buttons.html
   left_text="For technical details, see our organization’s"
   left_label="Research output" left_url="/research/publications/"
   right_text="For broader educational resources, see"
   right_label="Learning & Community" right_url="/team/community/" %}
