<template>
	<div class="sequence-block">
		<h3 class="sequence-badge" :style="{ color: badgeColor }">
			{{ badge }}
		</h3>
		<h2>{{ title }}</h2>
		<div class="sequence-timeline">
			<!-- Chaque enfant doit être un <TimelineItem> -->
			<slot />
		</div>
	</div>
</template>

<script setup>
defineProps({
	badge: { type: String, default: 'Séquence' },
	badgeColor: { type: String, default: '#4895ef' },
	title: { type: String, required: true },
});
</script>

<style scoped>
.sequence-block {
	padding: 1rem 2rem;
}

.sequence-badge {
	font-family: 'Bebas Neue', sans-serif;
	font-size: 1.3rem;
	letter-spacing: 0.25em;
	text-transform: uppercase;
	margin-bottom: 0.5rem;
}

.sequence-block h2 {
	font-family: 'Bebas Neue', sans-serif;
	font-size: 2.8rem;
	color: #ffffff;
	margin: 0 0 1.5rem;
}

.sequence-timeline {
	display: flex;
	flex-direction: column;
	gap: 0.9rem;
	padding-left: 1.5rem;
	border-left: 2px solid rgba(72, 149, 239, 0.6);
}
</style>
