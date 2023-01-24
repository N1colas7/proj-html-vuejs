<script>
export default {
    data() {
        return {
            activeSlide:0,
            slideJumbo:[
                {
                    Image:"../assets/img/home1_slide_2_bg.jpg",
                    Text:"d",
                    button:"d",
                },
                {
                    Image:"../assets/img/home1_slide_one_bg.jpg",
                    Text:"d",
                    button:"d",
                },
                {
                    Image:"../assets/img/home1_slide_three_bg_2.jpg",
                    Text:"d",
                    button:"d",
                },
            ]
        }
    }   
}

</script>
<template lang="">
    <div class="slider-jumbo">
        <img src="slideJumbo[activeSlide].Image" :alt="slideJumbo[activeSlide].Text">
        <h3>{{ slideJumbo[activeSlide].Text}}</h3>
    </div>
</template>
<style lang="scss">
    .slider-jumbo{
        width: 100%;
    }
</style>