<script setup>
import { computed } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()
const currentPage = computed(() => Number(route.params.no) || 1)

const REFUS_MAP = { 13: 1, 14: 2, 16: 3, 22: '∞' }

const count = computed(() => {
  const keys = Object.keys(REFUS_MAP)
    .map(Number)
    .filter(k => k <= currentPage.value)
    .sort((a, b) => b - a)
  return keys.length > 0 ? REFUS_MAP[keys[0]] : 0
})
</script>

<template>
  <div class="refus-counter">
    <span class="refus-icon">🚪</span>
    <span class="refus-x">✖</span>
    <span class="refus-count">{{ count }}</span>
  </div>
</template>

<style scoped>
.refus-counter {
  position: fixed;
  top: 20px;
  right: 20px;
  display: flex;
  align-items: center;
  gap: 4px;
  background: rgba(0, 0, 0, 0.5);
  border: 1px solid rgba(255, 255, 255, 0.15);
  border-radius: 8px;
  padding: 5px 12px;
  font-size: 0.85rem;
  color: #ffffff;
  z-index: 9999;
  backdrop-filter: blur(6px);
  user-select: none;
  pointer-events: none;
}
.refus-x { color: #e63946; font-size: 0.7rem; }
.refus-count { font-family: 'Bebas Neue', sans-serif; font-size: 1.1rem; letter-spacing: 0.05em; }
</style>
