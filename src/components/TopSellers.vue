<script>
export default {
    data() {
        return {
            ActiveCategories:Array,
            ActiveSlide:0,
            TopMan:[
                {
                    img:"/img/black_elegant_leather_jacket.jpg",
                    title:"Black Leather Jacket",
                    subtitle:"Men,Jackets,Jeans",
                    price:"$235 $200",
                },
                {
                    img:"/img/black_leather_suit.jpg",
                    title:"Black Leather Suit",
                    subtitle:"Men,Jackets",
                    price:"$176",
                },
                {
                    img:"/img/blue_jacket_and_white_stripe_tee.jpg",
                    title:"Blue Jacket & Stripe Tee",
                    subtitle:"Men,Jackets,Suits",
                    price:"$580",
                },
                {
                    img:"/img/blue_leather_jacket.jpg",
                    title:"Modern Black Leather Suit",
                    subtitle:"Men,Jackets",
                    price:"$96",
                },
            ],
            TopWomen:[
                {
                    img:"/img/spring_printed_dress.jpg",
                    title:"Spring Printed Dress",
                    subtitle:"Dress,Women",
                    price:"$47",
                },
                {
                    img:"/img/modern_love_tee.jpg",
                    title:"Modern Love Tee",
                    subtitle:"T-shirt,Women",
                    price:"$68",
                },
                {
                    img:"/img/black_leather_jacket.jpg",
                    title:"Black Jacket",
                    subtitle:"Women,Jackets",
                    price:"$125",
                },
                {
                    img:"/img/hipster_black_top.jpg",
                    title:"Hipster Black Top",
                    subtitle:"T-Shirts,Women",
                    price:"$57",
                },
            ],
            TopAccessories:[
            {
                    img:"/img/casual_leather_belts.jpg",
                    title:"casual Leather Belts",
                    subtitle:"Accessories,men",
                    price:"$65",
                },
                {
                    img:"/img/leather_gloves.jpg",
                    title:"Leather Gloves",
                    subtitle:"Accessories,Gloves,Men,Women",
                    price:"$68",
                },
                {
                    img:"/img/modern_leather_boots.jpg",
                    title:"Modern Leather Boots",
                    subtitle:"Accessories,Men,Miscellaneous,Shoes",
                    price:"$50 $30",
                },
                {
                    img:"/img/brown_dress_shoes.jpg",
                    title:"Brown Dress Shoes",
                    subtitle:"Accessories,Women,Miscellaneous,Shoes",
                    price:"$46 $36",
                },
            ],
        }
        },
        mounted(){
            this.ActiveCategories = this.TopMan;
        },
        methods: {
            displayWomen(){
                this.ActiveCategories = this.TopWomen;
            },
            displayMan(){
                this.ActiveCategories = this.TopMan;
            },
            displayAccessories(){
                this.ActiveCategories = this.TopAccessories;
            },
        },
    }
</script>
<template lang="">
    <div class="TopSellers">
        <h1>Featured Products</h1>
        <p>Must have products from our top sellers</p>
            <div class="btn-group ButtonTopSellers" role="group" aria-label="Basic outlined example">
                <button type="button" class="btn btn-outline-secondary" @click="displayMan()">Man</button>
                <button type="button" class="btn btn-outline-secondary" @click="displayWomen()">Women</button>
                <button type="button" class="btn btn-outline-secondary" @click="displayAccessories()">Accessories</button>
            </div>
            <div class="ContainTop">
                <div class="card">
                    <div class="contentTop">
                        <img v-for="(item, index) in ActiveCategories" :key="index" :src="item.img" alt="img">
                    </div>
                    <div class="TopText">
                        <h3 v-for="(item, index) in ActiveCategories" :key="index">{{item.title}}</h3>
                    </div>
                    <div class="subtitle">
                        <p v-for="(item, index) in ActiveCategories" :key="index">{{item.subtitle}}</p>
                    </div>
                    <div class="price">
                        <p v-for="(item, index) in ActiveCategories" :key="index">{{item.price}}</p>
                    </div>
                </div>
            </div>    
    </div>
</template>
<style lang="scss">
    .TopSellers{
        margin-top: 50px;
        h1,p{
            text-align: center;
        }
        .ButtonTopSellers{
            display:flex;
        }
        .ContaintTop{
            display: flex;
            .card{
                width:calc(100% / 4);
                margin-left: 60px;
            }
        }
        img{
            width:calc(100% / 4);
        }
        .TopText{
            display: flex;
            justify-content: space-around;
        }
        .subtitle{
            display: flex;
            justify-content: space-around;
            opacity: 0.7;
        }
        .price{
            display: flex;
            justify-content: space-around;
        }
        
    }
</style>


