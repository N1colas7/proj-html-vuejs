<script>
import FirstPartFoot from './FirstPartFoot.vue';
export default {
    data() {
        return {
           
        }
    },
}
</script>
<template lang="">
    <div class="container-fluid mt-5">
        <div class="row grey d-flex justify-content-around">
            <div class="col-6 d-flex center justify-content-evenly">
                <span class="message"><i class="fa-solid fa-envelope"></i></span>
                <h3>Suscribe now and get special offers</h3>
            </div>
            <div class="col-6 d-flex center justify-content-evenly">
                <input class="form-control" type="text" placeholder="Insert you email" aria-label="default input example">
                <button type="button" class="btn btn-primary">Send</button>
            </div>
        </div>
    </div>
</template>
<style lang="scss">
    .row{
        height: 300px;
    }
    .grey{
        background-color: rgb(46, 50, 56);
        color:white;
    }
    .center{
        align-items: center;
    }
    .message{
        padding: 2%;
        background-color: rgb(37, 37, 37);
        border-radius: 50%;
        font-size: 30px;
    }
</style>