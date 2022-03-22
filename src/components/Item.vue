<template>
	<div class="card my-2 item-todo">
		<p>{{ tache }}</p>
		<div v-on:click="suppTache" class="btn-supr btn btn-danger">X</div>
	</div>
</template>

<script>
export default {
	name: "Item",
	props: ["tache", "suppTache"],
};
</script>

<style scoped>
.item-todo {
	position: relative;
	padding: 20px 60px 20px 30px;
	font-size: 20px;
	height: 88px;
}

.card {
	list-style-type: none;
	border: 1px solid black;
	width: 70%;

	margin: 15px 0;
	display: flex;
	justify-content: space-between;
	flex-direction: row;
	align-items: baseline;
}
</style>
