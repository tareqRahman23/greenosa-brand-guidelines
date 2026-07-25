<script>
  import SectionLabel from './SectionLabel.svelte';

  const base = import.meta.env.BASE_URL;

  const values = [
    ['Purpose', 'Remove friction between data, strategy and execution.'],
    ['Mission', 'Fuse AI, human creativity and community presence into connected growth.'],
    ['Vision', 'Help brands move at the speed of intelligence and culture.'],
    ['Promise', 'Create campaigns that are seen on screens and felt in streets.']
  ];

  const pillars = ['AI-first systems', 'Cultural influence', 'On-ground activation', 'Integrity in execution'];

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
      <p>Greenosa is an AI-first hybrid marketing agency connecting intelligence, creativity and culture — across screens, streets and communities.</p>
    </div>

    <div class="strategy-brief">
      <div class="strategy-brief__headline reveal">
        <span>Strategic identity</span>
        <h3>AI-FIRST.<br />HUMAN-LED.<br /><em>FULLY INTEGRATED.</em></h3>
      </div>
      <div class="strategy-brief__body reveal">
        <blockquote>“Where intelligence meets integration — across screens and streets.”</blockquote>
        <p>For progressive brands reaching Bangladesh’s youth and trend-forward consumers, Greenosa unifies predictive intelligence, influencer networks and high-footfall activations into one agile growth system.</p>
        <div class="pillar-list">
          {#each pillars as pillar, index}
            <span><i>0{index + 1}</i>{pillar}</span>
          {/each}
        </div>
      </div>
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

    <div class="brand-story">
      <div class="brand-story__intro reveal">
        <span>The Greenosa world</span>
        <h3>CONNECTED BY DESIGN.<br /><em>FELT IN REAL LIFE.</em></h3>
        <p>People-first imagery shows the full journey: insight becomes an idea, an idea enters culture, and culture becomes measurable action.</p>
      </div>

      <div class="brand-story__grid">
        <figure class="brand-story__image brand-story__image--studio reveal">
          <img src={`${base}assets/greenosa-studio-intelligence.jpg`} alt="Young Bangladeshi strategists collaborating in a Greenosa-inspired creative studio" loading="lazy" />
          <figcaption><span>01 / Intelligence</span><strong>Human creativity, informed by data.</strong></figcaption>
        </figure>

        <figure class="brand-story__image brand-story__image--campus reveal">
          <img src={`${base}assets/greenosa-campus-activation.jpg`} alt="Young people engaging with an interactive campus activation in Bangladesh" loading="lazy" />
          <figcaption><span>02 / Streets</span><strong>Participation you can see and feel.</strong></figcaption>
        </figure>

        <article class="signal-card reveal">
          <div class="signal-card__top"><span>Connected signal</span><strong>LIVE / 01</strong></div>
          <svg viewBox="0 0 520 170" role="img" aria-label="A rising signal connecting insight, culture and action">
            <path class="signal-grid" d="M0 30H520M0 85H520M0 140H520" />
            <path class="signal-line" d="M8 139 C75 132,92 108,142 116 S218 52,273 79 S352 112,397 47 S463 28,512 12" />
            <circle cx="8" cy="139" r="5" /><circle cx="273" cy="79" r="5" /><circle cx="512" cy="12" r="5" />
          </svg>
          <div class="signal-card__metrics"><span><b>Insight</b>Predict</span><span><b>Culture</b>Connect</span><span><b>Action</b>Measure</span></div>
        </article>

        <figure class="brand-story__image brand-story__image--creator reveal">
          <img src={`${base}assets/greenosa-cultural-influence.jpg`} alt="A Bangladeshi creator producing a campaign on a Dhaka rooftop" loading="lazy" />
          <figcaption><span>03 / Screens</span><strong>Culture moving through connected media.</strong></figcaption>
        </figure>
      </div>
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
