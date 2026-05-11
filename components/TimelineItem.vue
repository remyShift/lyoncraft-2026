<template>
	<div class="timeline-item" :class="variantClass">
		<div class="tl-dot" :class="dotClass" :style="dotStyle" />
		<div class="tl-content">
			<slot />
		</div>
	</div>
</template>

<script setup>
import { computed } from 'vue';

const props = defineProps({
	/**
	 * 'default'  → dot bleu, fond neutre
	 * 'blocked'  → dot rouge, fond rouge, signale un refus/blocage
	 * 'insight'  → dot doré, fond doré, signale une révélation/pattern
	 */
	variant: { type: String, default: 'default' },
});

const variantClass = computed(() => ({
	'timeline-blocked': props.variant === 'blocked',
	'timeline-insight': props.variant === 'insight',
}));

const dotClass = computed(() => ({
	'tl-dot-red': props.variant === 'blocked',
	'tl-dot-gold': props.variant === 'insight',
}));

// Pas de style inline nécessaire — les couleurs sont gérées par les classes
const dotStyle = computed(() => ({}));
</script>

<style scoped>
.timeline-item {
	display: flex;
	align-items: flex-start;
	gap: 1rem;
	padding: 0.8rem 1rem;
	border-radius: 6px;
	background: rgba(72, 149, 239, 0.1);
	border: 1px solid rgba(72, 149, 239, 0.3);
}

.timeline-blocked {
	background: color-mix(in srgb, var(--color-door-red) 5%, transparent);
	border: 1px solid color-mix(in srgb, var(--color-door-red) 20%, transparent);
}

.timeline-insight {
	background: color-mix(in srgb, var(--color-door-gold) 5%, transparent);
	border: 1px solid
		color-mix(in srgb, var(--color-door-gold) 20%, transparent);
}

/* Dot */
.tl-dot {
	width: 10px;
	height: 10px;
	border-radius: 50%;
	background: var(--color-door-blue);
	flex-shrink: 0;
	margin-top: 5px;
}

.tl-dot-red {
	background: var(--color-door-red);
	box-shadow: 0 0 8px
		color-mix(in srgb, var(--color-door-red) 50%, transparent);
}
.tl-dot-gold {
	background: var(--color-door-gold);
	box-shadow: 0 0 8px
		color-mix(in srgb, var(--color-door-gold) 50%, transparent);
}

/* Contenu injecté via slot */
.tl-content {
	flex: 1;
}

:deep(p) {
	margin: 0;
	font-size: 1.2rem;
	line-height: 1.5;
	color: var(--text-primary);
}

:deep(strong) {
	color: var(--text-accent);
	font-weight: 600;
}

/* strong dans insight → couleur or */
.timeline-insight :deep(strong) {
	color: var(--color-door-gold);
}
</style>
