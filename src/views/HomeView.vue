<template>
  <div class="home-page">
    <section class="row">
      <RouterLink
        v-for="(product, index) in this.products.topRow "
        :key="index"
        :to="{ name: 'detail', params: {id: product.id} }">
        <ProductCard
          :title="product.title"
          :imgSources="product.images.m"
          :curentlyPrinting="product.curentlyPrinting"
          :stock="product.stock"
        ></ProductCard>
      </RouterLink>
    </section>

    <section class="icons">
      <div class="icon-container">
      </div>
      <p style="letter-spacing:10vw; margin-left: 10vw; font-weight:600;">trika bias</p>
    </section>

    <!-- <section class="row-full-width">
      <ProductCard
        class="full-row-item"
        :imgSources="[`src/assets/images/logo.jpg`]"
        style="text-align: center;"
      ></ProductCard>
    </section> -->
  </div>
</template>

<script>
  import ProductCard from '../components/ProductCard.vue'
  import ProductData from '../data/db.json'
  import Card from '../components/Card.vue'
  export default{
    components: {
      ProductCard,
      Card
    },
    data() {
    return {
      products: ProductData,
    }
  },
  }
</script>

<style scoped>
.home-page{
  max-width: 1440px;
  margin: 0 auto;
}
.row{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: .5rem;
}
a{
  color: black;
  text-decoration: none;
}
.icons{
  display: flex;
  flex-direction: column;
  justify-content: center;

  font-family: 'Courier New', Courier, monospace;
  font-size: large;
  text-align: center;
}
.icon-container{
  width: 320px;
  height: 78px;

  margin: .5rem auto;

  background-image: url(/src/components/icons/samolepka_1.svg);
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.icon-container:hover{
  background-image: url(/src/components/icons/samolepka_1_hover.svg);
}

@media screen and (max-width: 750px){
  .row {
    display: block;
  }
  .row-item{
    margin: 0 3rem;
  }
}
</style>