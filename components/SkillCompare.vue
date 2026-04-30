<template>
  <div class="skill-slide">
    <div class="skill-number" :style="{ color: colorHex }">{{ number }}</div>
    <h2>{{ title }}</h2>

    <div class="skill-cols">
      <!-- Colonne gauche : contexte d'origine (vente) -->
      <div class="skill-col">
        <div class="skill-context">{{ leftContext }}</div>
        <slot name="left" />
      </div>

      <div class="skill-arrow" :style="{ color: colorHex }">→</div>

      <!-- Colonne droite : parallèle avec le code — révélée au clic -->
      <div
        v-click
        class="skill-col skill-col-right"
        :style="{
          borderColor: `${colorHex}4d`,
          background: `${colorHex}0d`,
        }"
      >
        <div class="skill-context">{{ rightContext }}</div>
        <slot name="right" />
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  number:       { type: String, required: true },  // '01', '02', '03'
  title:        { type: String, required: true },
  colorHex:     { type: String, default: '#52b788' },
  leftContext:  { type: String, default: 'En vente' },
  rightContext: { type: String, default: 'En mission' },
})
</script>

<style scoped>
.skill-slide {
  padding: 1rem 2rem;
}

.skill-number {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 5rem;
  line-height: 1;
  opacity: 0.3;
}

.skill-slide h2 {
  font-size: 2.6rem;
  margin: 0.2rem 0 1.5rem;
  font-family: 'Bebas Neue', sans-serif;
  color: #ffffff;
}

.skill-cols {
  display: flex;
  align-items: center;
  gap: 1.5rem;
}

.skill-col {
  flex: 1;
  background: rgba(255, 255, 255, 0.04);
  border-radius: 8px;
  padding: 1.2rem;
  border: 1px solid rgba(255, 255, 255, 0.08);
}

.skill-col-right {
  border-width: 1px;
  border-style: solid;
}

.skill-context {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 0.9rem;
  letter-spacing: 0.2em;
  color: #8faac3;
  margin-bottom: 0.5rem;
}

/* Les <p> injectés via slot */
:deep(p) {
  font-size: 1.05rem;
  line-height: 1.6;
  margin: 0;
  color: #e8f0fe;
}

.skill-arrow {
  font-size: 2rem;
  flex-shrink: 0;
}
</style>
