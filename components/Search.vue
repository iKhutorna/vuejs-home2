
<template>
	<div class="search">
		<input class="search__field" v-model="changed">
	</div>
</template>


<style scoped lang="scss">
  .search {
    width: 300px;
    margin: 30px auto;
    display: block;
    &__field {
      width: 100%;
      padding: 10px;
    }
  }
</style>

<script>
export default {
	data () {
		return {
			changed: '',
		}
	},
	watch: {
	    changed(value) {
	        this.$emit('search', value);
	    }
	}
}
</script>