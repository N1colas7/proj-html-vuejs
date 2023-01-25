<script>
export default {
    props:{
    TopRatedProducts:Array,
    RecentPosts:Array,
    ButtonList:Array,
   } 
}
</script>
<template lang="">
    <div class="container-fluid">
        <div class="row">
            <div class="col-3 d-flex flex-column">
                <img src="/img/classic_shop_logo_footer.png" alt="img">
                 <ul class="mt-4">
                    <li>12345 North Main Street</li>
                    <li>New York,NY 555555</li>
                    <li>Phone: 1.800.555.6789</li>
                    <li>Email: info@company.com</li>
                    <li>Web: Theme-fusion.com</li>
                 </ul>
                 <div class="social">
                    <i class="fa-brands fa-facebook-f mx-2"></i>
                    <i class="fa-brands fa-twitter mx-2"></i>
                    <i class="fa-brands fa-instagram mx-2"></i>
                    <i class="fa-brands fa-youtube mx-2"></i>
                 </div>
            </div>
            <div class="col-3 ">
                <h4>Top Rated Products</h4>
                    <div class="card-products mt-4">
                        <div class="text d-flex justify-content-around margin" v-for="(item, index) in TopRatedProducts" :key="index">
                       <div> 
                            <p >{{item.name}}</p>
                            <p >{{item.price}}</p>
                        </div>
                        <div>
                            <img class="size" :src="item.img" alt="img">
                        </div>
                        </div>
                        
                    </div>
            </div>
            <div class="col-3 ">
                <h4>Recent Posts</h4>
                <div class="card-products">
                    <div v-for="(item, index) in RecentPosts" :key="index">
                        <div class="img-recent">
                            <img :src="item.img" alt="img">
                        </div>
                        <div class="text">
                            <p>{{item.title}}</p>
                            <p class="opacity">{{item.text}}</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-3 ">
                <h4>Tags</h4>
                <div class="card-button">
                    <button class="btn-array" v-for="(item, index) in ButtonList" :key="index">{{item.name}}</button>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss">
    .container-fluid{
        background-color: rgb(43, 46, 50);
        color:white;
        height: 600px;
    }
    .social{
        margin-left: 30px;
    }
    .size{
        width:80px
    }
    .margin{
        margin-bottom: 20px;
    }
    .opacity{
        opacity: 0.5;
        font-size: 12px;
    }
    .card-button{
        flex-wrap: wrap;
    }
    .btn-array{
        height: 50px;
        width: 80px;
        margin: 2px;
        background-color: transparent;
        border: 1px solid white;
        color: white;
    }
</style>