<template>
  <div class="content">
  <header>
    <div class="wrapper">
      <NavBar></NavBar>
    </div>
  </header>

  <main>
    <RouterView />
  </main>

  <footer>
    <img class="footer-img" src="./components/icons/robot.svg" alt="robot">
    <ul class="footer-list">
      <li>
        <img src="./components/icons/ikona_email_1.svg" alt="email icon" width="25">
        <!-- <p>objednavky@trikabias.cz</p> -->
        <a href="mailto:trika.bias@gmail.com"> trika.bias@gmail.com </a> 
      </li>
      <li>
        <img src="./components/icons/ikona_instagram_1.svg" alt="instagram icon" width="25">
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
  
}
header {
  padding: 1rem;
}
main{
  margin-bottom: 120px;
}
footer{
  position: relative;

  background-color: var(--green-color);
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
