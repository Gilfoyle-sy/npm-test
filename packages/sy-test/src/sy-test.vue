<template lang="html">
	<div 
		class="sy-test"
	>
		<div class="btn-switch" @click="switchModal()">Switch</div>
		<div v-show="isShow" class="modal red"></div>
		<div v-show="!isShow" class="modal blue"></div>
	</div>
</template>

<script>
	export default {
		name: 'syTest',
		data() {
			return {
				isShow: false
			}
		},
		methods: {
			switchModal () {
				const vm = this;
				vm.isShow = !vm.isShow
			}
		},
	}

</script>

<style lang='scss' scoped>
	.sy-test {
		.btn-switch {
			width: 70px;
			height: 30px;
			font-size: 14px;
			font-weight: bold;
			color: green;
		}
		.modal {
			width: 70px;
			height: 70px;
			border-radius: 50%;
			&.red {
				border: 1px solid red;
				box-shadow: 0 0 3px 3px gray;
				background: red;
			}
			&.blue {
				border: 1px solid blue;
				box-shadow: 0 0 3px 3px gray;
				background: blue;
			}
		}
	}
</style>