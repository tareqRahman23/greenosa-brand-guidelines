<script>
  import SectionLabel from './SectionLabel.svelte';

  const base = import.meta.env.BASE_URL;

  const colors = [
    ['#59C32D', 'Green', 'Momentum and optimism'],
    ['#00219D', 'Blue', 'Scale and digital confidence'],
    ['#2A2A2A', 'Charcoal', 'Structure and authority'],
    ['#F6F7F2', 'Off-white', 'Space and clarity']
  ];
</script>

<section class="identity" id="identity">
  <div class="identity-heading dark-section">
    <div class="section-inner">
      <SectionLabel number="02" title="Identity system" />
      <h2 class="display-heading reveal">IDENTITY, <br />BUILT TO <em>MOVE.</em></h2>
      <p class="identity-heading__copy reveal">Three marks, one connected system — designed to adapt without losing recognition.</p>
    </div>
  </div>

  <div class="logo-grid">
    <article class="logo-panel logo-panel--light reveal">
      <span>Primary lockup</span>
      <img src={`${base}assets/greenosa-wordmark-dark-transparent.png`} alt="Greenosa Digital primary lockup" />
      <p>Use for most brand communications.</p>
    </article>
    <article class="logo-panel logo-panel--dark reveal">
      <span>Reversed lockup</span>
      <img src={`${base}assets/greenosa-wordmark-light-transparent.png`} alt="Greenosa Digital reversed lockup" />
      <p>Use on dark photography and color fields.</p>
    </article>
    <article class="logo-panel logo-panel--symbol reveal">
      <span>G symbol</span>
      <img src={`${base}assets/greenosa-g.png`} alt="Greenosa G symbol" />
      <p>Use when space is limited or the brand is already known.</p>
    </article>
  </div>

  <div class="clearspace-band">
    <div class="clearspace-copy reveal">
      <span>Protect visibility at every size</span>
      <h3>CLEARSPACE<br />IS PART OF<br />THE MARK.</h3>
    </div>
    <div class="clearspace-demo reveal">
      <span class="measure measure--top">X</span>
      <span class="measure measure--left">X</span>
      <img src={`${base}assets/greenosa-wordmark-dark-transparent.png`} alt="Greenosa Digital clearspace example" />
      <div class="min-size"><strong>160 px</strong><span>minimum digital width</span></div>
    </div>
  </div>

  <div class="palette">
    {#each colors as color}
      <article class="color-swatch reveal" style={`--swatch:${color[0]}`}>
        <div><strong>{color[0]}</strong><span>{color[1]}</span></div>
        <p>{color[2]}</p>
      </article>
    {/each}
  </div>

  <div class="type-system dark-section">
    <div class="section-inner">
      <SectionLabel number="04" title="Typography" />
      <div class="type-grid">
        <article class="type-card reveal">
          <span>Display / Campaign headlines</span>
          <h3 class="akira">AKIRA<br />EXPANDED</h3>
          <p>Short, high-impact statements. Uppercase, generous and decisive.</p>
        </article>
        <article class="type-card reveal">
          <span>Primary / Editorial and body</span>
          <h3 class="forma">Forma DJR</h3>
          <p>Titles, subheads, body copy and captions. Built for clarity at every scale.</p>
        </article>
        <article class="type-sample reveal">
          <span>Sample</span>
          <h3>IDEAS <em>BUILT FOR</em> IMPACT</h3>
        </article>
      </div>
    </div>
  </div>
</section>
