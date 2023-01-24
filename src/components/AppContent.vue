<script>
export default {
    data() {
        return {
            activeSlide:0,
            slideJumbo:[
                {
                    id:1,
                    Image:"/img/home1_slide_2_bg.jpg",
                    Title:"Online Store",
                    Text:"Set Your Products With Style",
                    ButtonOne:"Men",
                    ButtonTwo:"Women",
                },
                {
                    id:2,
                    Image:"/img/home1_slide_one_bg.jpg",
                    Title:"Avada Classic Shop",
                    Text:"Show Your Products With Style",
                    ButtonOne:"Get Avada Now!",
                    ButtonTwo:"",
                },
                {
                    id:3,
                    Image:"/img/home1_slide_three_bg_2.jpg",
                    Title:"Brand New Arrivals",
                    Text:"New Collection from New York",
                    ButtonOne:"View All",
                    ButtonTwo:"Lookbook",
                },
            ]
        }
    },
    methods: {
        nextSlide(){
          this.activeSlide++;
      },
      prevSlide(){
          this.activeSlide--;
      }
}
}

</script>
<template lang="">
    <div class="slider-jumbo">
        <div :style="'background-image:url('+slideJumbo[activeSlide].Image+')'" :alt="slideJumbo[activeSlide].Text" class="slideContent">
            <h1>{{ slideJumbo[activeSlide].Title}}</h1>
            <p>{{slideJumbo[activeSlide].Text}}</p>
        <div class="buttonSlideChange">
            <div class="prev" v-if="slideJumbo.length!=0">
                <button type="button" class="btn btn-dark" @click="prevSlide">indietro</button>
            </div>
            <div class="next" v-if="slideJumbo.length-1!=activeSlide">
                <button type="button" class="btn btn-dark" @click="nextSlide">avanti</button>    
            </div>
        </div>
        <div class="buttonSlide">
            <button type="button" class="btn btn-light mx-3">{{ slideJumbo[activeSlide].ButtonOne }}</button>
            <button type="button" class="btn btn-light mx-3">{{ slideJumbo[activeSlide].ButtonTwo }}</button>
        </div>
        </div>
    </div>

</template>
<style lang="scss">
    .slider-jumbo{
        width: 100%;
        color: white;
        .slideContent{
            height: 600px;
            background-position: center;
            display: flex;
            justify-content: center;
            flex-direction: column;
            h1,p{
                text-align: center;
            }
        }
    }
    .buttonSlideChange{
        display: flex;
        justify-content: space-between;
        
    }
    .buttonSlide{
        opacity: 0.6;
        text-align: center;
        
    }

</style>