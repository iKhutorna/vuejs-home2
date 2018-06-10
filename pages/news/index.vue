
<template>
  <div class="news">
  	<div class="news__head">
  		<Head/>
  	</div>
  	<div class="container">
      <div class="search">
        <input class="search__field" v-model="query">
      </div>
      <Article v-for="item in computedList" :key='item.id' v-bind:title="item.title" v-bind:date="item.date"  v-bind:text="item.text"/>
  	</div>
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


// @ is an alias to /src
import Head from '@/components/Head.vue'
import Article from '@/components/Article.vue'

var articles = [ 
  {
    id: 1,
    title: 'Year in review: Our Favourite Apps from 2012',
    date: 'Posted on March 3, 2013',
    text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Deleniti, nesciunt unde error amet autem, obcaecati est molestias dignissimos dolore nam non saepe rem iure aspernatur, tempore quos! Laudantium, aperiam amet. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor fugiat nulla sunt quisquam ipsam ut ducimus minima nostrum sapiente, enim, odio optio accusantium, aperiam suscipit maiores. Vero iusto est, debitis.'
  }, 
  {
    id: 2,
    title: 'Hello',
    date: 'Posted on March 3, 2013', 
    text: 'Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text.'
  },
  {
    id: 3,
    title: 'MTZ worldwide is always',
    date: 'Posted on March 3, 2013', 
    text: 'MTZ worldwide is always in pole position when it comes to engine development and technology. Packed with detailed reports from research and development for highly specialised engineers. MTZ worldwide is an essential reading for technology-oriented management in the automotive industry with a special focus on engine development. Expert authors from industry and technology report on research projects.' 
  }
];


export default {
  components: {
    Head,
    Article
  },
  data () {
    return {
      query: '',
      list: articles
    }
  },
  computed: {
    computedList: function () {
      var vm = this;
      return this.list.filter(function (item) {
        return item.title.toLowerCase().includes(vm.query.toLowerCase()) || item.text.toLowerCase().includes(vm.query.toLowerCase());
      });
    }
  },
}
</script>
