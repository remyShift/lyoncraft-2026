<template>
  <div class="timeline-item" :class="variantClass">
    <div class="tl-dot" :class="dotClass" :style="dotStyle" />
    <div class="tl-content">
      <slot />
    </div>
  </div>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
  /**
   * 'default'  → dot bleu, fond neutre
   * 'blocked'  → dot rouge, fond rouge, signale un refus/blocage
   * 'insight'  → dot doré, fond doré, signale une révélation/pattern
   */
  variant: { type: String, default: 'default' },
})

const variantClass = computed(() => ({
  'timeline-blocked': props.variant === 'blocked',
  'timeline-insight': props.variant === 'insight',
}))

const dotClass = computed(() => ({
  'tl-dot-red':  props.variant === 'blocked',
  'tl-dot-gold': props.variant === 'insight',
}))

// Pas de style inline nécessaire — les couleurs sont gérées par les classes
const dotStyle = computed(() => ({}))
</script>

<style scoped>
.timeline-item {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
  padding: 0.8rem 1rem;
  border-radius: 6px;
  background: rgba(255, 255, 255, 0.03);
}

.timeline-blocked {
  background: rgba(230, 57, 70, 0.05);
  border: 1px solid rgba(230, 57, 70, 0.2);
}

.timeline-insight {
  background: rgba(252, 191, 73, 0.05);
  border: 1px solid rgba(252, 191, 73, 0.2);
}

/* Dot */
.tl-dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: #4895ef;
  flex-shrink: 0;
  margin-top: 5px;
}

.tl-dot-red  { background: #e63946; box-shadow: 0 0 8px rgba(230, 57, 70, 0.5); }
.tl-dot-gold { background: #fcbf49; box-shadow: 0 0 8px rgba(252, 191, 73, 0.5); }

/* Contenu injecté via slot */
.tl-content {
  flex: 1;
}

:deep(p) {
  margin: 0;
  font-size: 1.05rem;
  line-height: 1.5;
  color: #e8f0fe;
}

:deep(strong) {
  color: #ffffff;
  font-weight: 600;
}

/* strong dans insight → couleur or */
.timeline-insight :deep(strong) {
  color: #fcbf49;
}
</style>
