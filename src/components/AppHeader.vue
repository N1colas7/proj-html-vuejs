<script>
export default {
   props:{
    navHead:Array,
   } 
}
</script>
<template>
   <div class="head">
        <div class="container">
            <div class="row">
                <div class="col-6 d-flex">
                    <i class="fa-brands fa-facebook-f mx-2"></i>
                    <i class="fa-brands fa-twitter mx-2"></i>
                    <i class="fa-brands fa-instagram mx-2"></i>
                    <i class="fa-brands fa-youtube mx-2"></i>
                </div>
                <div class="col-6 d-flex justify-content-around">
                    <div class="left-head">
                        <p>Shopping Cart</p>
                    </div>
                    <div class="left-head bord-left">
                        <p>
                            My Account <i class="fa-solid fa-caret-down"></i>
                        </p>
                    </div>
                    <div class="left-head bord-left d-flex">
                        <span class="mx-1"><i class="fa-solid fa-cart-shopping"></i></span>
                        <span class="mx-1">Cart</span>
                        <span class="mx-2"><i class="fa-solid fa-caret-down"></i></span>
                    </div>

                </div>
            </div>
        </div>
   </div>
   <div class="main">
        <div class="row d-flex justify-content-around">
            <div class="col-6">
                <img src="../assets/img/classic_shop_logo1x.png" alt="image">
            </div>
            <div class="col-6">
                <ul>
                    <li v-for="(item , index) in navHead" :key="index">{{ item.name }}</li>
                </ul>    
            </div>
        </div>   
   </div>
</template>
<style lang="scss">
    .head{
        border-bottom: 1px solid rgb(209, 207, 207);
        margin-top: 10px;
    }
    .bord-left{
        border-left: 1px solid rgb(209, 207, 207);;
    }
    .main{
        padding: 10px;
    }
</style>