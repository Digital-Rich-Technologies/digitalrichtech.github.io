<template>
  <div class="page-features">
    <section class="features-intro">
      <div class="container">
        <h1>Features</h1>
        <p class="lead">Venue Genius is the coordination hub for your team: staff communicate from the floor, coordinators see progress and orchestrate from one place.</p>
      </div>
    </section>

    <section class="feature-block">
      <div class="container container--wide">
        <div class="feature-block__content">
          <div class="feature-block__media">
            <div class="feature-image-placeholder" aria-hidden="true">
              <span class="feature-image-placeholder__label">Feature image 1</span>
              <span class="feature-image-placeholder__hint">Add image (e.g. 800×500)</span>
            </div>
          </div>
          <div class="feature-block__text">
            <h2>Real-time staff communication</h2>
            <p>Staff report status from the floor; everyone sees it instantly. No more radio chaos or missed handoffs.</p>
            <p class="feature-block__fill">Add more copy, bullets, or links here as needed.</p>
          </div>
        </div>
      </div>
    </section>

    <section class="feature-block feature-block--alt">
      <div class="container container--wide">
        <div class="feature-block__content feature-block__content--reverse">
          <div class="feature-block__media">
            <div class="feature-image-placeholder" aria-hidden="true">
              <span class="feature-image-placeholder__label">Feature image 2</span>
              <span class="feature-image-placeholder__hint">Add image (e.g. 800×500)</span>
            </div>
          </div>
          <div class="feature-block__text">
            <h2>Coordinator dashboard</h2>
            <p>One place to watch progress and direct the team. See who’s where, what’s done, and what’s next.</p>
            <p class="feature-block__fill">Add more copy, bullets, or links here as needed.</p>
          </div>
        </div>
      </div>
    </section>

    <section class="feature-block">
      <div class="container container--wide">
        <div class="feature-block__content">
          <div class="feature-block__media">
            <div class="feature-image-placeholder" aria-hidden="true">
              <span class="feature-image-placeholder__label">Feature image 3</span>
              <span class="feature-image-placeholder__hint">Add image (e.g. 800×500)</span>
            </div>
          </div>
          <div class="feature-block__text">
            <h2>Built for events</h2>
            <p>Catering, venues, bar staffing: one place to run the show. Designed for how event teams actually work.</p>
            <p class="feature-block__fill">Add more copy, bullets, or links here as needed.</p>
          </div>
        </div>
      </div>
    </section>

    <section class="feature-more">
      <div class="container">
        <h2>More to come</h2>
        <p class="feature-more__fill">Use this section for additional feature highlights, screenshots, or links. You can add more blocks above by duplicating a <code>feature-block</code> and updating the placeholder and text.</p>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
useHead({
  title: 'Features — Venue Genius',
  meta: [{ name: 'description', content: 'Event staff coordination, real-time communication, and progress visibility for coordinators.' }]
})
</script>

<style scoped>
.page-features { padding-bottom: 3rem; }

.features-intro {
  padding: 2.5rem 0;
}
.features-intro h1 { margin: 0 0 0.5rem; font-size: 1.75rem; }
.features-intro .lead {
  margin: 0;
  color: var(--drt-text-muted);
  max-width: 50ch;
}

.container--wide { max-width: 960px; }

.feature-block {
  padding: 2.5rem 0;
  border-top: 1px solid #e5e7eb;
}
.feature-block--alt { background: #fafafa; }

.feature-block__content {
  display: grid;
  gap: 1.5rem;
  align-items: start;
}
@media (min-width: 640px) {
  .feature-block__content {
    grid-template-columns: 1fr 1fr;
  }
  .feature-block__content--reverse {
    direction: rtl;
  }
  .feature-block__content--reverse > * {
    direction: ltr;
  }
}

.feature-block__media { min-width: 0; }
.feature-image-placeholder {
  aspect-ratio: 16 / 10;
  background: #e5e7eb;
  border: 2px dashed #9ca3af;
  border-radius: 8px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 0.25rem;
  color: #6b7280;
  font-size: 0.875rem;
}
.feature-image-placeholder__label {
  font-weight: 600;
  color: #4b5563;
}
.feature-image-placeholder__hint {
  font-size: 0.75rem;
  opacity: 0.9;
}

.feature-block__text { min-width: 0; }
.feature-block__text h2 {
  margin: 0 0 0.5rem;
  font-size: 1.35rem;
  font-weight: 600;
}
.feature-block__text p {
  margin: 0 0 0.5rem;
  color: var(--drt-text-muted);
  line-height: 1.6;
}
.feature-block__fill {
  font-size: 0.9rem;
  color: #9ca3af;
  font-style: italic;
}

.feature-more {
  padding: 2.5rem 0;
  border-top: 1px solid #e5e7eb;
  background: #f8fafc;
}
.feature-more h2 { margin: 0 0 0.5rem; font-size: 1.2rem; }
.feature-more__fill {
  margin: 0;
  color: var(--drt-text-muted);
  font-size: 0.95rem;
}
.feature-more code {
  background: #e5e7eb;
  padding: 0.1rem 0.35rem;
  border-radius: 4px;
  font-size: 0.9em;
}
</style>
