<template>
  <div class="price-selector" role="group" aria-label="Billing period">
    <button
      type="button"
      class="price-selector__option"
      :class="{ 'price-selector__option--active': modelValue === 'monthly' }"
      :aria-pressed="modelValue === 'monthly'"
      @click="select('monthly')"
    >
      Monthly
    </button>
    <button
      type="button"
      class="price-selector__option"
      :class="{ 'price-selector__option--active': modelValue === 'yearly' }"
      :aria-pressed="modelValue === 'yearly'"
      @click="select('yearly')"
    >
      Yearly
    </button>
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{ modelValue: 'monthly' | 'yearly' }>()
const emit = defineEmits<{ 'update:modelValue': [value: 'monthly' | 'yearly'] }>()

function select(value: 'monthly' | 'yearly') {
  emit('update:modelValue', value)
}
</script>

<style scoped>
.price-selector {
  display: inline-flex;
  background: #f3f4f6;
  border-radius: 9999px;
  padding: 4px;
  gap: 2px;
}
.price-selector__option {
  padding: 0.5rem 1.25rem;
  border: none;
  border-radius: 9999px;
  font-size: 0.95rem;
  font-weight: 500;
  background: transparent;
  color: var(--drt-text-muted);
  cursor: pointer;
  transition: background 0.15s, color 0.15s;
}
.price-selector__option:hover {
  color: var(--drt-text);
}
.price-selector__option--active {
  background: #fff;
  color: var(--drt-text);
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.06);
}
</style>
