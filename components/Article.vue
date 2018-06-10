<template>

  <div class="section">
    <div class="section__title">
      <p>
        {{title}}
      </p>
    </div>
    <div class="section__textual">
          <p>{{date}}</p>
    </div>
      <div class="section__photo">
        <img src="~assets/image-1.png">
      </div>
      <div class="section__textual section__textual_l">
        <p>{{text}}</p>
      </div>
      <div class="section__btn-more">
        <ReadMore>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nihil nesciunt pariatur, similique aliquam natus in non magnam, quod ipsum velit eaque sapiente. Eveniet aliquam molestias excepturi, vel, nostrum quaerat optio!</ReadMore>
      </div>
  </div>
  
</template>

<script>

import ReadMore from '@/components/ReadMore.vue'


export default {
  name: 'Article',
  props: ['title', 'date', 'text'],
  components: {
    ReadMore
  }
}

</script>

