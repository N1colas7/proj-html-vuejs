<script>
import FirstPartFoot from './FirstPartFoot.vue';
import MainFoot from './MainFoot.vue';
import EndFoot from './EndFoot.vue';
export default {
    components:{
        FirstPartFoot,
        MainFoot,
        EndFoot,
    },
    data() {
        return {
    TopRatedProducts:[
          {
            name:"Leather Gloves",
            star:"",
            price:"$45",
            img:"/img/leather_gloves-120x156.jpg",
          },
          {
            name:"Black Leather Jacket",
            star:"",
            price:"$200",
            img:"/img/black_elegant_leather_jacket-120x156.jpg",
          },
          {
            name:"Spring Printed Dress",
            star:"",
            price:"$47",
            img:"/img/spring_printed_dress-120x156.jpg",
          },
          {
            name:"Blue Leather Jacket",
            star:"",
            price:"$87",
            img:"/img/blue_leather_jacket-120x156.jpg",
          },
        ],
        RecentPosts:[
            {
                img:"/img/post_img_12-300x188.jpg",
                title:"Aenean lobortis sapien enim viverra",
                text:"Markup, News, Trends",
            },
            {
                img:"/img/post_img_11-300x188.jpg",
                title:"Duis ac massa semper maximus",
                text:"Fashion, News, Special Offers, Trends",
            },
        ],
        ButtonList:[
            {
                name:"Black"
            },
            {
                name:"Boots"
            },
            {
                name:" Brown"
            },
            {
                name:"Casual"
            },
            {
                name:"D&G"
            },
            {
                name:"Fabric"
            },
            {
                name:"flowers"
            },
            {
                name:"Grey"
            },
            {
                name:"hat"
            },
            {
                name:"hipster"
            },
            {
                name:"lines"
            },
            {
                name:"red"
            },
            {
                name:"new york"
            },
            {
                name:"responsive"
            },
            {
                name:"summer"
            },
        ]
      }
    },
}
</script>
<template lang="">
    <FirstPartFoot />
    <MainFoot :TopRatedProducts= TopRatedProducts :RecentPosts=RecentPosts :ButtonList=ButtonList />
    <EndFoot />
</template>
<style lang="scss">
    
</style>