<template>
  <article class="addon-card">
    <h3 class="addon-card__name">{{ name }}</h3>
    <p class="addon-card__desc">{{ description }}</p>
    <p class="addon-card__cta">
      <NuxtLink :to="ctaHref || '/contact'" class="addon-card__btn">{{ ctaText }}</NuxtLink>
    </p>
  </article>
</template>

<script setup lang="ts">
defineProps<{
  name: string
  description: string
  ctaText?: string
  ctaHref?: string
}>()
</script>

<style scoped>
.addon-card {
  padding: 1.25rem;
  background: #fff;
  border: 1px solid #e5e7eb;
  border-radius: 8px;
  display: flex;
  flex-direction: column;
  height: 100%;
}
.addon-card__name {
  margin: 0 0 0.5rem;
  font-size: 1.1rem;
  font-weight: 600;
}
.addon-card__desc {
  margin: 0 0 1rem;
  font-size: 0.95rem;
  color: var(--drt-text-muted);
  line-height: 1.5;
  flex: 1;
}
.addon-card__cta { margin: 0; }
.addon-card__btn {
  display: inline-block;
  padding: 0.5rem 1rem;
  border-radius: 6px;
  font-weight: 600;
  font-size: 0.9rem;
  text-decoration: none;
  background: #f3f4f6;
  color: var(--drt-text);
  border: 1px solid #e5e7eb;
}
.addon-card__btn:hover { background: #e5e7eb; }
</style>
