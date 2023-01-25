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
                    <div class="dropdown left-head">
                        <button class="btn dropdown-toggle" type="button" id="dropdownMenuButton1" data-bs-toggle="dropdown" aria-expanded="false">
                            Shopping Cart
                        </button>
                        </div>
                    <div class="dropdown left-head bord-left">
                        <button class="btn dropdown-toggle" type="button" id="dropdownMenuButton1" data-bs-toggle="dropdown" aria-expanded="false">
                            My Account
                        </button>
                        <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1">
                            <li><a class="dropdown-item" href="#">Setting</a></li>
                            <li><a class="dropdown-item" href="#">Account</a></li>
                            <li><a class="dropdown-item" href="#">Orders</a></li>
                        </ul>
                        </div>
                        <div class="dropdown left-head bord-left">
                        <button class="btn dropdown-toggle" type="button" id="dropdownMenuButton1" data-bs-toggle="dropdown" aria-expanded="false">
                            Cart
                        </button>
                        <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1">
                            <li><a class="dropdown-item" href="#">Folder</a></li>
                            <li><a class="dropdown-item" href="#">MyCart</a></li>
                        </ul>
                        </div>

                </div>
            </div>
        </div>
   </div>
   <div class="main">
        <div class="row d-flex">
            <div class="col-4">
                <img src="/img/classic_shop_logo1x.png" alt="image">
            </div>
            <div class="col-8">
                <ul>
                    <li class="" v-for="(item , index) in navHead" :key="index">
                        <div class="dropdown">
                        <button class="btn dropdown-toggle" type="button" id="dropdownMenuButton1" data-bs-toggle="dropdown" aria-expanded="false">
                            {{ item.name }}
                        </button>
                        <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1">
                            <li><a class="dropdown-item" href="#">Setting</a></li>
                            <li><a class="dropdown-item" href="#">Account</a></li>
                            <li><a class="dropdown-item" href="#">Orders</a></li>
                        </ul>
                        </div>
                    </li>
                    <li class=""><button type="button" class="btn btn-primary">Shop now</button></li>
                    <li class="ml-2"><i class="fa-solid fa-magnifying-glass"></i></li>
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
    ul{
        list-style: none;
            li{
                float: left;
            }
    }
</style>