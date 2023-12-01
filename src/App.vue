<script>
import AppHeader from './components/AppHeader.vue'
import AppContent from './components/AppContent.vue'
import AppFooter from './components/AppFooter.vue'


export default {
	components: {
		AppHeader,
		AppContent,
		AppFooter,
	}
}
</script>

<template>
	<header>
		<AppHeader />
	</header>

	<main class="main">
		<AppContent />
	</main>

	<footer>
		<AppFooter />
	</footer>
</template>

<style scoped>

</style>

