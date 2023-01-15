<template>
  <nav>
    <ul>
      <li>    
        <img class="home" src="./icons/obr.svg" alt="" width="100">
      </li>

      <li>
        <RouterLink to="/">
          <p>Domů</p>
        </RouterLink>
      </li>

      <li>
        <RouterLink to="/about">
          <p>O trikách</p>
        </RouterLink>
      </li>

      <li>
        <RouterLink to="/order">
          <p>Objednávka</p>
        </RouterLink>
      </li>
    </ul>
  </nav>
</template>

<script>
  export default {
      
  }
</script>

<style scoped>
ul{
  padding: 0;

  list-style: none;
  list-style-position: outside;
}
a{
  display: inline-block;
  text-decoration: none;
}
ul {
  display: flex;
  gap: 2rem;
  align-items: center;
  justify-content: center;

  width: 100%;
  margin-bottom: 1rem;

  font-size: 2rem;
  margin-top: 0rem;
}
ul p{
  color: black;
}
ul p:hover{
  color: var(--green-color);
  text-shadow: 1px 1px 2px red, 0 0 1em blue, 0 0 0.2em blue;
}

/* RESPONSIVE */
@media screen and (max-width: 750px){
  ul {
    display: block;

    margin-bottom: 1rem;
    margin-top: 0rem;

    padding-left: 2rem;

    font-size: 2rem;
  }
}
</style>