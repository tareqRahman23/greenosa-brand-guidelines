<script>
  import SectionLabel from './SectionLabel.svelte';

  const base = import.meta.env.BASE_URL;

  const principles = [
    ['One idea', 'Lead with one message'],
    ['Clear path', 'Guide the eye'],
    ['Room to move', 'Protect whitespace']
  ];
</script>

<section class="visual-world dark-section" id="visual-world">
  <div class="section-inner">
    <SectionLabel number="05" title="Visual world" />
    <div class="visual-heading reveal">
      <h2>OPTIMISTIC<br /><em>WORLDS.</em><br />HUMAN<br /><em>PURPOSE.</em></h2>
      <p>Use depth, motion, luminous detail and clear focal points to make digital possibility feel tangible.</p>
    </div>

    <div class="art-grid">
      <figure class="art-card art-card--flow reveal">
        <img src={`${base}assets/brand-world-flow.jpg`} alt="A luminous connected path moving through an optimistic digital world" />
        <figcaption><strong>Immersive and energetic</strong><span>Make possibility tangible.</span></figcaption>
      </figure>
      <figure class="art-card art-card--platform reveal">
        <img src={`${base}assets/brand-world-platform.jpg`} alt="A connected digital platform shown as an optimistic cosmic world" />
        <figcaption><strong>Systems made visible</strong><span>Show people, tools and communities in motion.</span></figcaption>
      </figure>
    </div>

    <div class="principles">
      {#each principles as principle, index}
        <article class="principle reveal">
          <span>0{index + 1}</span>
          <h3>{principle[0]}</h3>
          <p>{principle[1]}</p>
          <i aria-hidden="true">✦</i>
        </article>
      {/each}
    </div>
  </div>
</section>
