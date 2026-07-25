<script>
  import SectionLabel from './SectionLabel.svelte';

  const base = import.meta.env.BASE_URL;

  const steps = [
    ['Hook', 'Earn attention'],
    ['Proof', 'Support the claim'],
    ['Action', 'Make the next step obvious']
  ];
</script>

<section class="applications" id="applications">
  <div class="application-intro dark-section">
    <div class="section-inner">
      <SectionLabel number="06" title="Applications" />
      <div class="application-layout">
        <div class="campaign-frame reveal">
          <img src={`${base}assets/campaign-cover.png`} alt="Greenosa Digital campaign application: Where influence meets impact" />
        </div>
        <div class="campaign-copy reveal">
          <span>Social and digital</span>
          <h2>BUILT TO<br />STOP, INFORM<br />AND <em>MOVE.</em></h2>
          <p>Build one clear message per frame, then adapt the composition to the platform rather than simply resizing it.</p>
        </div>
      </div>

      <div class="impact-steps">
        {#each steps as step, index}
          <article class="impact-step reveal">
            <span>0{index + 1}</span>
            <h3>{step[0]}</h3>
            <p>{step[1]}</p>
          </article>
        {/each}
      </div>

      <div class="copy-system reveal">
        <span>Copy system</span>
        <h3>SHORT ENOUGH TO <em>MOVE,</em><br />SPECIFIC ENOUGH TO <em>TRUST.</em></h3>
        <div class="copy-lines">
          <p>Turn attention into action.</p>
          <p>Ideas that travel further.</p>
          <p>Built for the next move.</p>
          <p>Make the moment matter.</p>
        </div>
      </div>
    </div>
  </div>

  <div class="finale">
    <div class="finale__star">✦</div>
    <h2>MAKE THE<br />NEXT MOVE<br /><em>MATTER.</em></h2>
    <div class="finale__bottom">
      <p>Integrated ideas that connect attention to action.</p>
      <img src={`${base}assets/greenosa-wordmark-dark-transparent.png`} alt="Greenosa Digital" />
    </div>
  </div>

  <footer class="site-footer">
    <span>© 2026 Greenosa Digital</span>
    <a href="#top">Back to top ↑</a>
    <span>Version 1.0 / July 2026</span>
  </footer>
</section>
