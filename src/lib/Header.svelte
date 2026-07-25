<script>
  let open = false;
  const base = import.meta.env.BASE_URL;

  const links = [
    ['Foundation', '#foundation'],
    ['Identity', '#identity'],
    ['Visual world', '#visual-world'],
    ['Applications', '#applications']
  ];

  function closeMenu() {
    open = false;
  }
</script>

<header class="site-header">
  <a class="brand-link" href="#top" aria-label="Greenosa Digital home" on:click={closeMenu}>
    <img src={`${base}assets/greenosa-wordmark-light-transparent.png`} alt="Greenosa Digital" />
  </a>

  <nav class="desktop-nav" aria-label="Primary navigation">
    {#each links as link}
      <a href={link[1]}>{link[0]}</a>
    {/each}
  </nav>

  <a class="download-link" href={`${base}Greenosa_Brand_Guidelines.pdf`} download>
    <span>Download guide</span>
    <svg viewBox="0 0 24 24" aria-hidden="true">
      <path d="M12 3v12m0 0 5-5m-5 5-5-5M5 21h14" />
    </svg>
  </a>

  <button class="menu-toggle" class:open aria-label="Toggle navigation" aria-expanded={open} on:click={() => (open = !open)}>
    <span></span><span></span>
  </button>
</header>

{#if open}
  <div class="mobile-menu">
    <div class="mobile-menu__meta">Greenosa Digital / Brand Guidelines</div>
    <nav aria-label="Mobile navigation">
      {#each links as link, index}
        <a href={link[1]} on:click={closeMenu}><span>0{index + 1}</span>{link[0]}</a>
      {/each}
    </nav>
    <a class="mobile-menu__download" href={`${base}Greenosa_Brand_Guidelines.pdf`} download on:click={closeMenu}>Download PDF ↘</a>
  </div>
{/if}
