
<template>
  <div class="news">
  	<div class="news__head">
  		<Head/>
  	</div>
  	<div class="container">
  		<div class="section">
  			<div class="section__title">
  				<p>
  					Year in review: Our Favourite Apps from 2012
  				</p>
  			</div>
  			<div class="section__textual">
          		<p>Posted on March 3, 2013</p>
  			</div>
	        <div class="section__photo">
	          <img src="~assets/image-1.png">
	        </div>
	        <div class="section__textual section__textual_l">
	          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Deleniti, nesciunt unde error amet autem, obcaecati est molestias dignissimos dolore nam non saepe rem iure aspernatur, tempore quos! Laudantium, aperiam amet. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor fugiat nulla sunt quisquam ipsam ut ducimus minima nostrum sapiente, enim, odio optio accusantium, aperiam suscipit maiores. Vero iusto est, debitis.</p>
	        </div>
	        <div class="section__btn-more">
            <ReadMore>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nihil nesciunt pariatur, similique aliquam natus in non magnam, quod ipsum velit eaque sapiente. Eveniet aliquam molestias excepturi, vel, nostrum quaerat optio!</ReadMore>
	        </div>
  		</div>
  		<div class="section">
  			<div class="section__title">
  				<p>
  					Year in review: Our Favourite Apps from 2012
  				</p>
  			</div>
  			<div class="section__textual">
          		<p>Posted on March 3, 2013</p>
  			</div>
	        <div class="section__photo">
	          <img src="~assets/image-2.png">
	        </div>
	        <div class="section__textual section__textual_l">
	          <p>Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. Another text. </p>
	        </div>
          <div class="section__btn-more">
            <ReadMore>transition2</ReadMore>
          </div>
  		</div>
  		<div class="section section_no-m-b">
  			<div class="section__title">
  				<p>
  					Year in review: Our Favourite Apps from 2012
  				</p>
  			</div>
  			<div class="section__textual">
          		<p>Posted on March 3, 2013</p>
  			</div>
	        <div class="section__photo">
	          <img src="~assets/image-3.png">
	        </div>
	        <div class="section__textual section__textual_l">
	          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Deleniti, nesciunt unde error amet autem, obcaecati est molestias dignissimos dolore nam non saepe rem iure aspernatur, tempore quos! Laudantium, aperiam amet. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor fugiat nulla sunt quisquam ipsam ut ducimus minima nostrum sapiente, enim, odio optio accusantium, aperiam suscipit maiores. Vero iusto est, debitis.</p>
	        </div>
  		</div>
  	</div>

  </div>
</template>

<script>
// @ is an alias to /src
import Head from '@/components/Head.vue'
import ReadMore from '@/components/ReadMore.vue'


export default {
  name: 'home',
  components: {
  	Head,
    ReadMore
  }
}
</script>
