<script>
  import SectionLabel from './SectionLabel.svelte';

  const values = [
    ['Purpose', 'Make brand influence useful, memorable and measurable.'],
    ['Mission', 'Create integrated communications that turn attention into meaningful action.'],
    ['Promise', 'Bold thinking, responsive partnership and work built for real-world impact.']
  ];

  const voice = [
    ['Bold', 'Speak with energy'],
    ['Curious', 'Make it accessible'],
    ['Agile', 'Stay credible'],
    ['Human', 'Invite participation']
  ];
</script>

<section class="foundation dark-section" id="foundation">
  <div class="section-inner">
    <SectionLabel number="01" title="Brand foundation" />
    <div class="foundation__intro reveal">
      <h2>MAKE BRAND <em>INFLUENCE</em><br />USEFUL, MEMORABLE<br />AND <em>MEASURABLE.</em></h2>
      <p>Greenosa connects brands, people and culture through ideas designed to move — across screens, streets and communities.</p>
    </div>

    <div class="value-grid">
      {#each values as value, index}
        <article class="value-item reveal">
          <span>0{index + 1}</span>
          <h3>{value[0]}</h3>
          <p>{value[1]}</p>
        </article>
      {/each}
    </div>

    <div class="voice-grid">
      <div class="voice-grid__lead reveal">
        <span>How Greenosa should feel</span>
        <h3>CONFIDENT,<br />NOT LOUD.</h3>
        <p>Inventive, not vague. Friendly, not casual. Fast, not careless.</p>
      </div>
      <div class="voice-list">
        {#each voice as item, index}
          <div class="voice-row reveal">
            <span>0{index + 1}</span>
            <strong>{item[0]}</strong>
            <p>{item[1]}</p>
            <svg viewBox="0 0 24 24" aria-hidden="true"><path d="M5 12h14m-5-5 5 5-5 5" /></svg>
          </div>
        {/each}
      </div>
    </div>
  </div>
</section>
