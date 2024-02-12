<template>
	<main>
		<h1>Vue Popups</h1>
		<button @click="() => TogglePopup()">Open Popup</button>
		
		<Popup 
			v-if="popupTriggers" 
			:TogglePopup="() => TogglePopup()">
			<h2>My Button Popup</h2>
		</Popup>
	</main>
</template>

<script setup>
import { ref } from 'vue';
import Popup from './components/Popup.vue';

		const popupTriggers = ref(false);

		const TogglePopup = () => {
			popupTriggers.value = !popupTriggers.value
		}

</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}
</style>
