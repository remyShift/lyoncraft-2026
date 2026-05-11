<template>
	<span class="tag" :class="`tag-${variant}`">
		<slot>{{ label }}</slot>
	</span>
</template>

<script setup>
defineProps({
	variant: { type: String, default: 'blue' }, // 'green' | 'blue' | 'red' | 'gold'
	label: { type: String, default: '' },
});
</script>

<style scoped>
.tag {
	display: inline-block;
	padding: 0.2rem 0.8rem;
	border-radius: 999px;
	font-family: 'Bebas Neue', sans-serif;
	font-size: 1.2rem;
	text-transform: uppercase;
}

.tag-green {
	background: var(--color-door-green-bg);
	color: var(--text-accent);
}
.tag-blue {
	background: var(--color-door-blue-bg);
	color: var(--text-accent);
}
.tag-red {
	background: var(--color-door-red-bg);
	color: var(--text-accent);
}
.tag-gold {
	background: var(--color-door-gold-bg);
	color: var(--text-accent);
}
</style>
