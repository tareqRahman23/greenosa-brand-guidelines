<script>
  import { onMount } from 'svelte';
  import { gsap } from 'gsap';
  import { ScrollTrigger } from 'gsap/ScrollTrigger';
  import Header from './lib/Header.svelte';
  import Foundation from './lib/Foundation.svelte';
  import Identity from './lib/Identity.svelte';
  import VisualWorld from './lib/VisualWorld.svelte';
  import Applications from './lib/Applications.svelte';

  const base = import.meta.env.BASE_URL;

  onMount(() => {
    gsap.registerPlugin(ScrollTrigger);
    const reduceMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;
    if (reduceMotion) return;

    const ctx = gsap.context(() => {
      gsap.from('.hero-line', {
        yPercent: 115,
        opacity: 0,
        duration: 1.15,
        stagger: 0.1,
        ease: 'power4.out',
        delay: 0.15
      });

      gsap.from('.hero-copy, .scroll-cue', {
        y: 20,
        opacity: 0,
        duration: 0.8,
        stagger: 0.12,
        ease: 'power3.out',
        delay: 0.8
      });

      gsap.to('.hero-mark', {
        rotation: 10,
        yPercent: 8,
        ease: 'none',
        scrollTrigger: { trigger: '.hero', start: 'top top', end: 'bottom top', scrub: 1 }
      });

      gsap.to('.hero-glow', {
        xPercent: 20,
        yPercent: 12,
        ease: 'none',
        scrollTrigger: { trigger: '.hero', start: 'top top', end: 'bottom top', scrub: 1.2 }
      });

      gsap.utils.toArray('.reveal').forEach((element) => {
        gsap.from(element, {
          y: 42,
          opacity: 0,
          duration: 0.9,
          ease: 'power3.out',
          scrollTrigger: { trigger: element, start: 'top 87%', once: true }
        });
      });

      gsap.utils.toArray('.art-card img').forEach((image) => {
        gsap.fromTo(image, { yPercent: -5, scale: 1.06 }, {
          yPercent: 5,
          scale: 1.06,
          ease: 'none',
          scrollTrigger: { trigger: image.parentElement, start: 'top bottom', end: 'bottom top', scrub: 1 }
        });
      });

      gsap.from('.finale', {
        clipPath: 'inset(0 50% 0 50%)',
        ease: 'power3.inOut',
        scrollTrigger: { trigger: '.finale', start: 'top 80%', end: 'top 25%', scrub: 1 }
      });
    });

    return () => ctx.revert();
  });
</script>

<svelte:head>
  <link rel="preload" href={`${base}assets/greenosa-wordmark-light-transparent.png`} as="image" />
</svelte:head>

<div class="page-shell" id="top">
  <Header />

  <main>
    <section class="hero dark-section">
      <div class="hero-glow" aria-hidden="true"></div>
      <img class="hero-mark" src={`${base}assets/greenosa-g.png`} alt="" aria-hidden="true" />
      <div class="hero-content">
        <h1>
          <span class="hero-line">WHERE</span>
          <span class="hero-line accent">INFLUENCE</span>
          <span class="hero-line">MEETS</span>
          <span class="hero-line accent">IMPACT.</span>
        </h1>
        <p class="hero-copy">Greenosa connects brands, people and culture<br />through ideas designed to move.</p>
        <a class="scroll-cue" href="#foundation">
          <svg viewBox="0 0 24 40" aria-hidden="true"><path d="M12 1v36m0 0 8-8m-8 8-8-8" /></svg>
          <span>Scroll to explore</span>
        </a>
      </div>
      <div class="hero-meta">
        <span>Brand guidelines</span>
        <span>Identity system / V1.0</span>
        <span>July 2026</span>
      </div>
    </section>

    <Foundation />
    <Identity />
    <VisualWorld />
    <Applications />
  </main>
</div>
