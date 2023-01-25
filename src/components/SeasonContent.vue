<script>
export default {
    
}
</script>
<template lang="">
    <div class="container-season">
        <div class="row-season">
            <div class="col Winter">
                <h1>Winter Collection</h1>
                <p>Stylish And Warm</p>
                <button type="button" class="btn btn-light">View More</button>
            </div>
            <div class="col Spring">
                <h1>Spring Collection</h1>
                <p>Brigth And Colorful</p>
                <button type="button" class="btn btn-light">View More</button>
            </div>
            <div class="col Autumn">
                <h1>Autumn Collection</h1>
                <p>Rich And COmfortable</p>
                <button type="button" class="btn btn-light">View More</button>
            </div>
        </div>
    </div>
</template>
<style lang="scss">
    .container-season{
        margin-top: 50px;
    }
    .row-season{
        display: flex;
    }
    .col{
        width: calc(100% / 3);
        text-align: center;
        height: 500px;
        color:white;
        
    }    
    .Winter{
        background-image: url('/img/winter_collection_bg.jpg');
        background-position: center;
        background-size: 500px;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        
    }
    .Spring{
        background-image: url('/img/spring_collection_bg.jpg');
        background-position: center;
        background-size: 500px;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        
    }
    .Autumn{
        background-image: url('/img/autumn_collection_bg.jpg');
        background-position: center;
        background-size: 500px;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
    }
    
</style>