<template>
	<div class="refus-counter">
		<span class="refus-icon">🚪</span>
		<span class="refus-x">✖</span>
		<span class="refus-count">{{ count }}</span>
	</div>
</template>

<script setup>
import { computed } from 'vue';
import { useNav } from '@slidev/client';

const { currentPage } = useNav();

const REFUS_MAP = { 13: 1, 14: 2, 16: 3, 22: '∞' };

const count = computed(() => {
	const keys = Object.keys(REFUS_MAP)
		.map(Number)
		.filter((k) => k <= currentPage.value)
		.sort((a, b) => b - a);
	return keys.length > 0 ? REFUS_MAP[keys[0]] : 0;
});
</script>

<style scoped>
.refus-counter {
	position: absolute;
	top: 18px;
	right: 20px;
	display: flex;
	align-items: center;
	gap: 5px;
	background: rgba(0, 0, 0, 0.55);
	border: 1px solid rgba(255, 255, 255, 0.15);
	border-radius: 8px;
	padding: 5px 12px;
	color: #ffffff;
	z-index: 200;
	user-select: none;
	pointer-events: none;
}
.refus-icon {
	font-size: 1rem;
	line-height: 1;
}
.refus-x {
	color: #e63946;
	font-size: 0.7rem;
	line-height: 1;
}
.refus-count {
	font-family: 'Bebas Neue', sans-serif;
	font-size: 1.2rem;
	letter-spacing: 0.05em;
	line-height: 1;
}
</style>
