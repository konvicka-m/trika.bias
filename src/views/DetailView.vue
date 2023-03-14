<template>
    <div class="detail-view">
        <section class="slide-show">
            <h1 class="title">{{ this.product.title }}</h1>

            <p 
                class="curently-printing printing"
                v-if="this.curentlyPrinting"
            >tisknem</p>

            <img 
                v-for="(image, index) in this.images"
                v-show="index === this.curentImageIndex"
                :key="index"
                class="image-slide"
                :src=image 
                :alt="'triko'">

            <p class="price"> {{ this.product.price + " CZK" }}</p>
        </section>

        <div class="buttons">
            <button 
                class="previous"
                @click="this.previousImage()"
            >&larr;</button>

            <p>{{ (this.curentImageIndex+1) + "/" + this.images.length }}</p>

            <button 
                class="next"
                @click="this.nextImage()"
            >&rarr;</button>
        </div>
        <!-- <p>{{ this.product }}</p>
        <p>{{ "proměnná images: " + this.images }}</p> -->
    </div>   
</template>

<script>
    import ProductData from '../data/db.json'
    export default {
        data() {
            return {
                product: ProductData.topRow[this.id-1],
                images: ProductData.topRow[this.id-1].images.m.concat(ProductData.topRow[this.id-1].detailImages),
                curentImageIndex: 0,
                curentlyPrinting: true
            }
        },
        props:{
            id: {
                default: 0
            },

        },
        methods: {
            nextImage() {
                if(this.curentImageIndex < this.images.length-1){
                    this.curentImageIndex ++
                }
            },
            previousImage() {
                if(this.curentImageIndex > 0){
                    this.curentImageIndex --
                }
            }
        },
    }
</script>

<style scoped>
.slide-show{
    position: relative;
    max-width: 700px;
    min-width: 500px;
    width: 50vw;
    margin: 0 25vw;
}
.title{
    color: springgreen;
    font-size: 3rem;
    position: absolute;
    bottom: 0;
    left: 0;

    transform-origin: bottom left;
    transform: rotate(-90deg);
}
.curently-printing{
    position: absolute;
    top: 0;
    right: 0;

    transform-origin: bottom right;
    transform: rotate(90deg) translateX(80%);
}
.printing{
    color: springgreen;
}
.not-printing{
    color: grey;
    text-shadow: 1px 1px 2px black;
    margin-top: 1rem;
}
.price{
    color: white;
    position: absolute;
    bottom: 0;
    right: 0;
    transform-origin: bottom right;
    transform: rotate(90deg) translate(-5%);
}
.buttons{
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 3rem;
}
button{
    color: white;
    font-size: 1.2rem;

    background: none;
    border: none;
}
button:hover{
    cursor: pointer;
    /* background-color: rgba(0, 0, 0, 0.313); */
    background-color: white;
    color: black;
    /* box-shadow: 1px 1px 2px red, 0 0 1em blue, 0 0 0.2em blue; */
    border-radius: 2rem;
}
.image-slide{
    width: 100%;
}
@media screen and (max-width: 750px){
    .slide-show{
        position: relative;
        width: 80vw;
        margin-left: 3rem;

        min-width: 200px;
    }
    .title{
        font-size: 1.5rem;
    }

@media screen and (max-width: 400px){
    .slide-show{
        position: relative;
        width: 80vw;
        margin: 0 2rem;

        min-width: 200px;
    }
    .title{
        font-size: 1.2rem;
    }
}
}
</style>