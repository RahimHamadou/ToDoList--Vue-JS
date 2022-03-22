<template>
	<div class="header-top">
		<p>{{ titre }}</p>
	</div>
</template>

<script>
export default {
	name: "header",
	data() {
		return {
			titre: "La ToDoList",
		};
	},
};
</script>

<style scoped>
.header-top {
	position: fixed;
	top: 0;
	right: 0;
	height: 50px;
	background: #333;
	color: #f1f1f1;
	width: 100%;
	text-align: center;
	line-height: 50px;
	font-size: 25px;

	margin: 0;
}
p {
	margin: 0 auto;
}
</style>
