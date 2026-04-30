<template>
  <span class="tag" :class="`tag-${variant}`">
    <slot>{{ label }}</slot>
  </span>
</template>

<script setup>
defineProps({
  variant: { type: String, default: 'blue' }, // 'green' | 'blue' | 'red' | 'gold'
  label:   { type: String, default: '' },
})
</script>

<style scoped>
.tag {
  display: inline-block;
  padding: 0.2rem 0.8rem;
  border-radius: 999px;
  font-family: 'Bebas Neue', sans-serif;
  font-size: 0.9rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
}

.tag-green { background: #2d6a4f; color: #52b788; }
.tag-blue  { background: #1e3a5f; color: #4895ef; }
.tag-red   { background: #9b2226; color: #e63946; }
.tag-gold  { background: #f77f00; color: #fcbf49; }
</style>
