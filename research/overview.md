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
          aria-controls="summary-compact-do summary-plain-do" aria-label="Plain English summary" hidden>
    <span class="summary-switch-knob"></span>
  </button>
  <div class="summary-text">
    <div class="summary-compact" id="summary-compact-do">
      <p>We model AI risk factors and safety mitigations in terms of AIXI variants, and develop the means to translate them to real AI agents. This enables rigorous testing of both the risk factors and the safety mitigations.</p>
    </div>
    <div class="summary-plain" id="summary-plain-do" hidden>
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
  // Each .summary-toggle switches between its compact and plain-English text.
  // Without JS the compact text shows and the switches and hint stay hidden.
  document.addEventListener('DOMContentLoaded', function () {
    document.querySelectorAll('.summary-hint').forEach(function (hint) { hint.hidden = false; });
    document.querySelectorAll('.summary-toggle').forEach(function (toggle) {
      var button = toggle.querySelector('.summary-switch');
      var compact = toggle.querySelector('.summary-compact');
      var plain = toggle.querySelector('.summary-plain');
      button.hidden = false;
      button.addEventListener('click', function () {
        var on = button.getAttribute('aria-checked') !== 'true';
        button.setAttribute('aria-checked', String(on));
        compact.hidden = on;
        plain.hidden = !on;
      });
    });
  });
</script>

## Why this approach?

Most AI research today sits in one of two categories:

- Methods that are fast and mathematically clean in narrow settings
- Methods that are practical for frontier applications but opaque to safety analysis.

Our core focus is the third intersection: methods that are **general** enough to describe powerful agents and amenable to mathematical **analysis** to support rigorous safety claims.

Aligning a hypothetical superintelligence requires a concerted effort in this historically neglected direction.

<img class="approach-diagram" src="{{ '/assets/img/aixi_venn_diagram_v4.svg' | relative_url }}" alt="Venn diagram of Fast, General and Analyzable methods: Frontier AI is Fast and General, Textbook RL is Fast and Analyzable, and AIXI, our focus, is General and Analyzable" />

<p class="summary-hint" hidden>Click the toggle below to switch between the compact and ‘plain English’ summaries.</p>

<div class="summary-toggle">
  <button type="button" class="summary-switch" role="switch" aria-checked="false"
          aria-controls="summary-compact-how summary-plain-how" aria-label="Plain English summary" hidden>
    <span class="summary-switch-knob"></span>
  </button>
  <div class="summary-text">
    <div class="summary-compact" id="summary-compact-how">
      <p>Thus, we formally examine behaviors, capabilities, risks and mitigations for idealized agents in fully general environments. We aim to port the most promising methods to modern LLM-based agents, and test principled hypotheses on these agents. Since our analyses are based on a very general model of superintelligence, we gain confidence that any experimentally validated conclusions will generalize and scale to future AI systems.</p>
    </div>
    <div class="summary-plain" id="summary-plain-how" hidden>
      <p>Just as physicists simplify the real world into idealised models, we study AI through an idealised mathematical model.</p>
      <p>AIXI is a theoretically perfect learner and perfect planner rolled into one. It considers every possible explanation of the world it’s in, works out which actions lead to the best outcome, and acts accordingly. We prove what must be true about this “perfect” agent’s behaviour across a huge range of possible environments.</p>
      <p>We then test whether the same patterns appear in today’s AI agents. Because AIXI is so general, conclusions that hold up in both are likely to apply to future, more powerful AI systems too.</p>
    </div>
  </div>
</div>

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
   left_text="For technical details, see:"
   left_label="Publications" left_url="/research/publications/"
   right_text="For broader educational resources, see:"
   right_label="Learning & Community" right_url="/team/community/" %}
