<template>
  <div class="page-home">
    <section class="hero">
      <div class="container">
        <p class="hero-product">Venue Genius — a product from Digital Rich Technologies</p>
        <h1>Keep your event staff in sync—in real time.</h1>
        <p class="lead">
          Venue Genius is the coordination hub for your team: staff communicate from the floor, coordinators see progress and orchestrate from one place. No more radio chaos or missed handoffs.
        </p>
        <p class="cta-primary">
          <NuxtLink to="/contact" class="btn">Get a demo or quote</NuxtLink>
        </p>
        <p class="byline">By <NuxtLink to="/about-us">Digital Rich Technologies</NuxtLink></p>
      </div>
    </section>

    <section class="benefits">
      <div class="container">
        <h2 class="visually-hidden">Why Venue Genius</h2>
        <ul class="benefits-list">
          <li><strong>Real-time communication</strong> — Staff report status from the floor; everyone sees it instantly.</li>
          <li><strong>Coordinator visibility</strong> — One dashboard to watch progress and direct the team.</li>
          <li><strong>Built for events</strong> — Catering, venues, bar staffing: one place to run the show.</li>
        </ul>
      </div>
    </section>

    <TrustedBy />

    <!-- Add-ons teaser - links to pricing -->
    <section class="addons-teaser">
      <div class="container">
        <h2 class="addons-teaser__title">Optional add-ons</h2>
        <p class="addons-teaser__text">Extend Venue Genius with Walkie Talkie, Location Aware Check-ins, and AI Event Summaries. <NuxtLink to="/pricing#add-ons">See add-ons</NuxtLink>.</p>
      </div>
    </section>

    <!-- Bottom CTA strip -->
    <section class="home-cta">
      <div class="container">
        <h2 class="home-cta__title">Get started with Venue Genius</h2>
        <div class="home-cta__links">
          <NuxtLink to="/contact" class="home-cta__btn home-cta__btn--primary">Contact us</NuxtLink>
          <NuxtLink to="/pricing" class="home-cta__btn">See pricing</NuxtLink>
          <NuxtLink to="/features" class="home-cta__btn">See features</NuxtLink>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
useHead({
  title: 'Venue Genius — Event staff coordination in real time',
  meta: [{ name: 'description', content: 'Keep event staff in sync in real time. Venue Genius is the coordination hub for your team—staff communicate from the floor, coordinators orchestrate from one place.' }]
})
</script>

<style scoped>
.page-home { padding-bottom: 0; }

.hero {
  padding: 3rem 0;
  text-align: center;
  background: var(--drt-gradient-hero, linear-gradient(135deg, #e0e7ff 0%, #fce7f3 50%, #e0e7ff 100%));
}
.hero-product {
  margin: 0 0 0.5rem;
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--drt-purple);
  text-transform: uppercase;
  letter-spacing: 0.04em;
}
.hero-product a { color: inherit; text-decoration: none; }
.hero h1 {
  margin: 0 0 1rem;
  font-size: clamp(1.5rem, 4vw, 2.25rem);
  font-weight: 700;
  letter-spacing: -0.02em;
  line-height: 1.25;
  max-width: 20ch;
  margin-left: auto;
  margin-right: auto;
}
.hero .lead {
  margin: 0 auto 1.5rem;
  max-width: 42ch;
  font-size: 1.1rem;
  color: var(--drt-text-muted);
  line-height: 1.6;
}
.hero .cta-primary { margin: 0 0 1rem; }
.hero .btn {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  background: var(--drt-purple);
  color: #fff;
  text-decoration: none;
  font-weight: 600;
  font-size: 1rem;
  border-radius: 6px;
}
.hero .btn:hover {
  background: var(--drt-purple-dark, #3b0764);
}
.hero .byline {
  font-size: 0.875rem;
  color: var(--drt-text-muted);
}
.hero .byline a { color: var(--drt-purple); font-weight: 500; }

.benefits {
  padding: 2.5rem 0;
  background: #fff;
}
.benefits-list {
  list-style: none;
  padding: 0;
  margin: 0;
  max-width: 40ch;
  margin: 0 auto;
}
.benefits-list li {
  margin-bottom: 1rem;
  padding-left: 1.5rem;
  position: relative;
  color: var(--drt-text-muted);
  line-height: 1.5;
}
.benefits-list li::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0.4em;
  width: 6px;
  height: 6px;
  background: var(--drt-accent-teal);
  border-radius: 50%;
}
.benefits-list li:last-child { margin-bottom: 0; }

.addons-teaser {
  padding: 2rem 0;
  border-top: 1px solid #e5e7eb;
  background: #fafafa;
  text-align: center;
}
.addons-teaser__title {
  margin: 0 0 0.5rem;
  font-size: 1.15rem;
  font-weight: 600;
}
.addons-teaser__text {
  margin: 0;
  font-size: 0.95rem;
  color: var(--drt-text-muted);
  max-width: 44ch;
  margin-left: auto;
  margin-right: auto;
}
.addons-teaser a { color: var(--drt-purple); font-weight: 500; }

.home-cta {
  padding: 2.5rem 0;
  border-top: 1px solid #e5e7eb;
  text-align: center;
}
.home-cta__title {
  margin: 0 0 1rem;
  font-size: 1.35rem;
  font-weight: 600;
}
.home-cta__links {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 0.75rem;
}
.home-cta__btn {
  display: inline-block;
  padding: 0.6rem 1.25rem;
  border-radius: 6px;
  font-weight: 600;
  font-size: 0.95rem;
  text-decoration: none;
  background: #f3f4f6;
  color: var(--drt-text);
  border: 1px solid #e5e7eb;
}
.home-cta__btn:hover { background: #e5e7eb; }
.home-cta__btn--primary {
  background: var(--drt-purple);
  color: #fff;
  border-color: var(--drt-purple);
}
.home-cta__btn--primary:hover { background: var(--drt-purple-dark); }

.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border: 0;
}
</style>
