<template>
    <div class="card">
        <figure>
            <!-- <div 
                class="image"
                :style="{ backgroundImage: 'url(' + imgSources[this.curentImgIndex] + ')'}"
            ></div> -->
            <div 
                class="image"
                v-for="(image, index) in imgSources"
                :key="index"
                :style="{ backgroundImage: 'url('+ image +')'}"
                v-show="this.curentImgIndex == index"
            ></div>

            <p 
                class="curently-printing printing"
                v-if="this.curentlyPrinting"
            >tisknem</p>
            <p
                class="curently-printing not-printing"
                v-else-if="!this.curentlyPrinting"
            >netiskneme</p>
        </figure>
        <div class="container">
            <h2>{{title}}</h2>
            <p v-if="text">{{ text }}</p>
            <p v-if="stock">skladem: {{ stock }}</p> 
            <!-- <p>{{this.num}}</p> -->
            <!-- SMAZAT -->
            <!-- <p>{{ imgSources }}</p> -->
        </div>
    </div>
</template>

<script>
// for(let i; i < this.imgSource.length; i++ ){
//     this.num = i
// }
    export default {
        data() {
            return {
                curentImgIndex: 0,
                num: 0,
            }
        },
        props:{
            imgSource:{
                default: "src/assets/images/2792px-The_Forest_Stream_MET_DP146457.jpg"
            },
            imgSources:{
                default: ["src/assets/images/2792px-The_Forest_Stream_MET_DP146457.jpg"],
                type: Array
            },
            title: '',
            curentlyPrinting:{
                default: false,
                type: Boolean
            },
            stock: '',
            text: " ",
        },
        methods: {
            switchImg() {
                if(this.curentImgIndex < (this.imgSources.length-1)){
                    this.curentImgIndex ++
                }else{
                    this.curentImgIndex = 0
                }
                
            }
        },
        mounted() {
            if (this.imgSources.length > 1){
                setInterval(() => {
                    this.switchImg()
                }, 3000);
            }
        }
    }
</script>

<style scoped>
    .card{
        border: solid 1px grey;
    }
    figure{
        height: 50vh;
        margin: 0;

        position: relative;
    }
    .curently-printing{
        position: absolute;
        top: 0;
        right: 0;

        transform: translate(35%, 200%) rotate(0.25turn);
    }
    .printing{
        color: var(--green-color);
        text-shadow: 1px 1px 2px red, 0 0 1em blue, 0 0 0.2em blue;
    }
    .not-printing{
        color: grey;
        text-shadow: 1px 1px 2px black;
        margin-top: 1rem;
    }
    .image{
        width: 100%;
        height: 100%;

        /* margin: 1rem; */

        /* border: dashed red .1rem; */
        /* box-shadow: .4rem .4rem .6rem rgba(0, 0, 0, 0.2); */

        /* background-image: url("src/assets/images/2792px-The_Forest_Stream_MET_DP146457.jpg"); */
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
    }
    .container{
        position: relative;
        bottom: 0.8rem;
    }
</style>