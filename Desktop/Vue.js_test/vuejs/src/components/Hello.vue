<template>
	<div>
		{{msg}}
		<form>
			<button>ADD TASK</button>
			<button>DELETE FINISHED TASKS</button>
			<p>input: <input type="text"></p>
			<p>task:</p>
		</form>
		<div class="task-list">
			<label class="task-list__item"><input type="checkbox"><button>EDIT</button>vue-router</label>
			<label class="task-list__item"><input type="checkbox"><button>EDIT</button>vuex</label>
			<label class="task-list__item"><input type="checkbox"><button>EDIT</button>vue-loader</label>
			<label class="task-list__item--checked"><input type="checkbox" checked><button>EDIT</button>awesome-vue</label>
		</div>
	</div>
</template>

<script>
export default {
	name: 'hello',
	data(){
		return {
			msg: 'Welcom to Your Vue.js App'
		}
	}
}
</script>

<style lang="scss" scoped>
@mixin flex-vender(){
	display: flex;
	display: -weblit-flex;
	display: -moz-flex;
	display: -ms-flex;
	display: -o-flex;
}
.task-list{
	@include flex-vender;
	flex-direction: column;
	align-items:center;
	&__item{
		width: 270px;
		text-align: left;
		$element: #{&};
		&--checked{
			@extend #{$element};
			color: #85a6c6;
		}
	}
}
</style>