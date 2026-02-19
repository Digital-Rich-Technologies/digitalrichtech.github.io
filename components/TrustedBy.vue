<template>
  <section class="trusted-by" aria-labelledby="trusted-by-heading">
    <div class="container">
      <h2 id="trusted-by-heading" class="visually-hidden">Trusted by</h2>
      <p class="trusted-by__text">Trusted by teams that run world-class events.</p>
      <div class="trusted-by__logos">
        <div v-for="i in logoCount" :key="i" class="trusted-by__logo-box" aria-hidden="true">
          <span class="trusted-by__logo-label">Logo {{ i }}</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
withDefaults(
  defineProps<{
    logoCount?: number
  }>(),
  { logoCount: 6 }
)
</script>

<style scoped>
.trusted-by {
  padding: 2rem 0;
  border-bottom: 1px solid #e5e7eb;
  background: #fafafa;
}
.trusted-by__text {
  text-align: center;
  margin: 0 0 1rem;
  font-size: 0.95rem;
  color: var(--drt-text-muted);
}
.trusted-by__logos {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1rem;
}
.trusted-by__logo-box {
  width: 120px;
  height: 48px;
  background: #e5e7eb;
  border-radius: 6px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #9ca3af;
  font-size: 0.75rem;
}
.trusted-by__logo-label { opacity: 0.9; }

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
