<template>
  <div class="page-contact">
    <!-- Banner -->
    <section class="page-banner">
      <div class="page-banner__placeholder" aria-hidden="true">
        <span class="page-banner__label">Contact banner image</span>
        <span class="page-banner__hint">Add image (e.g. 1200×400)</span>
      </div>
    </section>

    <section class="content">
      <div class="container">
        <h1>Contact</h1>
        <p><strong>Digital Rich Technologies</strong></p>
        <p class="address">
          Headquarters: Bamboo Royal Oak<br>
          220 S Main St, Royal Oak, MI 48067
        </p>
        <p>
          <a href="https://www.bamboocowork.com/locations/royal-oak" target="_blank" rel="noopener noreferrer">View our office at Bamboo Royal Oak</a> — photos, amenities, and location details.
        </p>
        <p class="cta">Contact us for partnerships, press, or product inquiries.</p>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
useHead({
  title: 'Contact — Venue Genius',
  meta: [{ name: 'description', content: 'Contact Digital Rich Technologies. HQ: Bamboo Royal Oak, 220 S Main St, Royal Oak, MI.' }]
})
</script>

<style scoped>
.page-contact { padding-bottom: 3rem; }

.page-banner {
  width: 100%;
  margin-bottom: 2rem;
}
.page-banner__placeholder {
  aspect-ratio: 3 / 1;
  min-height: 180px;
  background: #e5e7eb;
  border: 2px dashed #9ca3af;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 0.25rem;
  color: #6b7280;
  font-size: 0.875rem;
}
.page-banner__label { font-weight: 600; color: #4b5563; }
.page-banner__hint { font-size: 0.75rem; opacity: 0.9; }

.content { padding: 0; }
.content h1 { margin: 0 0 1rem; font-size: 1.75rem; }
.content p { margin: 0 0 0.75rem; color: var(--drt-text-muted); }
.address { margin: 0.25rem 0 0.75rem; }
.content a { color: var(--drt-purple); font-weight: 500; }
.cta { margin-top: 1rem; }
</style>
