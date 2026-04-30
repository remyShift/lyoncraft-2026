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
	background: #2d6a4f;
	color: white;
}
.tag-blue {
	background: #1e3a5f;
	color: white;
}
.tag-red {
	background: #9b2226;
	color: white;
}
.tag-gold {
	background: #f77f00;
	color: white;
}
</style>
