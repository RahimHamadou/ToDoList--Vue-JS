<template>
	<div id="app">
		<header-top></header-top>
		<contenu></contenu>
		<br />
	</div>
</template>

<script>
import Header from "./components/Header.vue";
import Contenu from "./components/Contenu.vue";

export default {
	name: "App",
	components: {
		"header-top": Header,
		contenu: Contenu,
	},
};
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	/* text-align: center; */
	color: #2c3e50;
	margin-top: 60px;

	/* background-position: center;
	background-size: cover; */
}
body {
	height: 100vh;
	background: #b24592; /* fallback for old browsers */
	background: -webkit-linear-gradient(to bottom, #f15f79, #b24592); /* Chrome 10-25, Safari 5.1-6 */
	background: linear-gradient(
		to bottom,
		#f15f79,
		#b24592
	); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}
</style>
