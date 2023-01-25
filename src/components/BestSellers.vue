<script>
import { defineComponent } from 'vue'
import { Carousel, Navigation, Slide } from 'vue3-carousel'

import 'vue3-carousel/dist/carousel.css'

export default defineComponent({
  name: 'Breakpoints',
  components: {
    Carousel,
    Slide,
    Navigation,
  },
  data: () => ({
    settings: {
      itemsToShow: 1,
      snapAlign: 'center',
    },
    breakpoints: {
      700: {
        itemsToShow: 3,
        snapAlign: 'center',
      },
      1024: {
        itemsToShow: 5,
        snapAlign: 'start',
      },
    },
}),
data() {
    return {
        SlideImg:[
        {
            img:"/img/black_elegant_leather_jacket-231x300.jpg",
            text:"img",
        },
        {
            img:"/img/spring_printed_dress-231x300.jpg",
            text:"img",
        },
        {
            img:"/img/modern_love_tee-200x260.jpg",
            text:"img",
        },
        {
            img:"/img/black_leather_jacket-231x300.jpg",
            text:"img",
        },
        {
            img:"/img/hipster_black_top-231x300.jpg",
            text:"img",
        },
        {
            img:"/img/black_leather_suit-200x260.jpg",
            text:"img",
        }

    ]    
    }
},
})
</script>
<template >
    <div class="container mt-5">
        <div class="row center">
                <h1>Best Seller</h1>
                <p>Must have products from our top sellers</p>
        </div>
    <Carousel :items-to-show="5" :wrap-around='true' :settings="settings" :breakpoints="breakpoints">
    <Slide v-for="slide in SlideImg" :key="slide">
      <div class="carousel__item">
        <img :src="slide.img" :alt="slide.text">
    </div>
    </Slide>
    <template #addons>
      <Navigation />
    </template>
  </Carousel>
  </div>
</template>
<style lang="scss">
    .center{
        text-align: center;
    }
</style>