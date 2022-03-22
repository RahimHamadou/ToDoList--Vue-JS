<template>
	<div class="container">
		<h1>{{ titre }}</h1>

		<form>
			<!-- Input pour remplir la tache a faire -->
			<div class="form-group">
				<label for="action">Action</label>
				<input
					id="action"
					v-model="formData.tache"
					type="text"
					class="form-control"
					placeholder="Une tache"
					required
				/>
			</div>
			<!-- Btn d'ajout -->
			<button v-on:click.prevent="addTache" class="btn btn-primary mt-5 mb-3">Creer une tache</button>
		</form>
		<!-- Liste des taches -->

		<ul>
			<li class="task-list" v-for="(tache, index) in taches" v-bind:key="index">
				<item v-bind:id="index" v-bind:tache="tache" v-bind:suppTache="suppTache"></item>
			</li>
		</ul>
	</div>
</template>

<script>
import Item from "./Item.vue";
export default {
	name: "Contenu",
	data() {
		return {
			titre: "Creer des taches",

			formData: {
				tache: "",
			},
			taches: ["Vue", "React", "Angular", "Node"],
		};
	},
	components: {
		item: Item,
	},

	methods: {
		addTache: function () {
			if (this.formData.tache == "") {
				alert("Remplir le champs svp");
			} else {
				this.taches.push(this.formData.tache);
				this.formData.tache = "";
				console.log(this.taches);
			}
		},
		// fonction qui cible l'id d'un element et l'id de son parent

		// methode splice sert en remove un element d'un tableau depuis un id, le 1 indique le nombre d'element a remove
		suppTache: function (e) {
			this.taches.splice(e.target.parentNode.id, 1);
		},
	},
};
</script>

<style>
.task {
	position: absolute;
}

ul {
	list-style-type: none;
	padding: 0;
}
.task-btn {
	position: relative;
	background: red;
	color: #f1f1f1;
	border-radius: 5px;
}
h1,
label {
	color: whitesmoke;
}
</style>
