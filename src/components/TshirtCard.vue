<template>
    <div class="tshirt-card">
        <img :src="tshirt.images.m[0]">
        <h2 class="title">
            {{ tshirt.title }}
        </h2>
        <p v-if="tshirt.curentlyPrinting" class="currently-printing">tiskneme</p> 
        <p v-else class="currently-printing">netiskneme</p>
        <p class="price">
            {{ tshirt.price }} CZK
        </p>

        <!-- <p>{{ tshirt }}</p> -->
    </div>
</template>

<script>
    export default {
        props: {
            tshirt: {
                type: Object,
            },
        },
        
    }
</script>

<style scoped>
.tshirt-card{
    position: relative;
    border: 1px solid grey;
    padding:1.2rem;
}
.title{
    position: absolute;
    bottom:.35rem; 
    margin: 0;
    font-size:2rem;
    font-weight:500;
    color: springgreen
}
.currently-printing{
    position:absolute; 
    top: 1rem; 
    right: 0; 
    transform-origin: bottom right; 
    transform: rotate(-90deg) translateX(2ch);
    color:springgreen
}
.price{
    position: relative;
    margin: 0;
    bottom: 0;
    left: 100%;
    right: 0;
    transform-origin: top left;
    transform: rotate(-90deg);
    color: rgb(255, 255, 255);
}
img{
    width: 100%;
}
</style>