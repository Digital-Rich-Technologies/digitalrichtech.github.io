<template>
  <article class="plan-card" :class="{ 'plan-card--recommended': recommended }">
    <div v-if="recommended" class="plan-card__badge">Recommended</div>
    <h3 class="plan-card__name">{{ name }}</h3>
    <p class="plan-card__price">
      <template v-if="price === 'Custom'">{{ price }}</template>
      <template v-else>{{ price }}{{ period }}</template>
    </p>
    <ul class="plan-card__features">
      <li v-for="(feature, i) in features" :key="i">
        <span class="plan-card__check" aria-hidden="true">✓</span>
        {{ feature }}
      </li>
    </ul>
    <p class="plan-card__cta">
      <NuxtLink
        v-if="ctaHref"
        :to="ctaHref"
        class="plan-card__btn"
        :class="{ 'plan-card__btn--primary': recommended }"
      >
        {{ ctaText }}
      </NuxtLink>
      <a
        v-else-if="ctaExternal"
        :href="ctaExternal"
        class="plan-card__btn"
        :class="{ 'plan-card__btn--primary': recommended }"
      >
        {{ ctaText }}
      </a>
    </p>
  </article>
</template>

<script setup lang="ts">
defineProps<{
  name: string
  price: string
  period?: string
  features: string[]
  ctaText: string
  ctaHref?: string
  ctaExternal?: string
  recommended?: boolean
}>()
</script>

<style scoped>
.plan-card {
  position: relative;
  padding: 1.5rem;
  background: #fff;
  border: 1px solid #e5e7eb;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  height: 100%;
}
.plan-card--recommended {
  border-color: var(--drt-purple);
  box-shadow: 0 0 0 2px rgba(91, 33, 182, 0.15);
}
.plan-card__badge {
  position: absolute;
  top: -10px;
  left: 1rem;
  background: var(--drt-purple);
  color: #fff;
  font-size: 0.75rem;
  font-weight: 600;
  padding: 0.2rem 0.5rem;
  border-radius: 4px;
}
.plan-card__name {
  margin: 0 0 0.5rem;
  font-size: 1.25rem;
  font-weight: 600;
}
.plan-card__price {
  margin: 0 0 1rem;
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--drt-text);
}
.plan-card__features {
  list-style: none;
  padding: 0;
  margin: 0 0 1.5rem;
  flex: 1;
}
.plan-card__features li {
  display: flex;
  align-items: flex-start;
  gap: 0.5rem;
  margin-bottom: 0.5rem;
  font-size: 0.95rem;
  color: var(--drt-text-muted);
}
.plan-card__check {
  color: var(--drt-accent-teal);
  flex-shrink: 0;
}
.plan-card__cta { margin: 0; }
.plan-card__btn {
  display: block;
  text-align: center;
  padding: 0.65rem 1rem;
  border-radius: 6px;
  font-weight: 600;
  font-size: 0.95rem;
  text-decoration: none;
  background: #f3f4f6;
  color: var(--drt-text);
  border: 1px solid #e5e7eb;
}
.plan-card__btn:hover {
  background: #e5e7eb;
}
.plan-card__btn--primary {
  background: var(--drt-purple);
  color: #fff;
  border-color: var(--drt-purple);
}
.plan-card__btn--primary:hover {
  background: var(--drt-purple-dark);
}
</style>
