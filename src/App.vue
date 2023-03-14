<template>
  <div class="content">
  <header>
    <section class="icons">
      <div class="icon-container">
      </div>
      <p style="letter-spacing:10vw; margin-left: 10vw; font-weight:600;">trika bias</p>
    </section>

    <div class="wrapper">
      <NavBar></NavBar>
    </div>
  </header>

  <main>
    <RouterView />
  </main>

  <footer>
    <!-- <img class="footer-img" src="./components/icons/robot.svg" alt="robot"> -->
    <ul class="footer-list">
      <li>
        <!-- <img src="./components/icons/ikona_email_1.svg" alt="email icon" width="25"> -->
        <!-- <p>objednavky@trikabias.cz</p> -->
        <a href="mailto:trika.bias@gmail.com"> trika.bias@gmail.com </a> 
      </li>
      <li>
        <!-- <img src="./components/icons/ikona_instagram_1.svg" alt="instagram icon" width="25"> -->
        <a href="https://www.instagram.com/trika.bias/">trika.bias</a>
      </li>
    </ul>
  </footer>
</div>
</template>

<script>
import { RouterLink, RouterView } from 'vue-router'
import NavBar from './components/NavBar.vue'
export default{
  components: {
    NavBar
  }
}
</script>

<style scoped>
.content{
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  background-color: rgb(24 24 27);
}
header {
  color: white;
  /* background-color: aqua; */
  padding: 1rem;
  padding-bottom: 0px;
  margin-bottom: 46px;
  border-bottom: solid 2px black;
}
.icons{
  display: flex;
  flex-direction: column;
  justify-content: center;

  font-family: 'Courier New', Courier, monospace;
  font-size: large;
  text-align: center;
  margin: 5rem 0;
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
main{
  margin-bottom: 120px;
  background-color: rgb(24 24 27);
}
footer{
  position: relative;

  background-color: black;
  color: rgb(255, 255, 255);

  font-size: smaller;

  padding: .5rem 1rem;
  margin-top: auto;
}
.footer-img{
  position: absolute;
  top: -110px;
  margin-left: 80%;
  margin-right: auto;
}
.footer-list{
  max-width: 1170px;
  margin: 1rem auto;
}
li{
  display: flex;
  gap: .5rem;
  align-items: center;

  margin-bottom: 0.3rem;
}
li a{
  color: white;
}

@media screen and (max-width: 400px){
  .footer-img{
    position: absolute;
    top: -110px;
    left: 0px;
    /* margin-left: 80%; */
    margin-right: auto;
  }
}
</style>
