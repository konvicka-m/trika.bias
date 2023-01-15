<template>
  <div class="about-page">

    <h1 class="uvodni-text">Hele, naše trika jsou <strong>bastl</strong>. Počítej s tím. Dole máš par bodů, abys věděl co kupuješ.</h1>

    <ul>
      <li class="container">
        <h1>S chybou počítáme</h1>
        <p>Děláme autorské trika u sebe doma. Nejsme tiskárna s profi vybavením. Chyba je pro nas nedílnou součástí tvorby. Prostě s ní počítáme. Jestli hledáš dokonale potištěné triko, jsi tu špatně.</p>
      </li>
      <li class="container">
        <h1>Jestli dostaneš triko na druhý den není jisté</h1>
        <p>Trika tisknem ve volném čase. Neboj, nebudeš čekat měsíc, ale do druhého dne to rozhodně nebude.</p>
      </li>
      <li class="container">
        <h1>Per trika maximálně na 40, jinak ti z potisku zbyde jenom vzpomínka</h1>
        <p>Když budeš prát trika často na vysokou teplotu, potisk ti dlouho nevydrží.</p>
      </li>
      <li class="container">
        <h1>Nejsme vždycky eco, bio, green, vege, ale pracujem na tom</h1>
        <p>Používáme barvy od Daler Rowney. Barvy jsou vodouředitelné bez rozpouštědel.</p>
      </li>
    </ul>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto&family=Space+Mono&display=swap');
.about-page{
  max-width: 900px;
  margin: 0 auto;
  padding: 0rem 3rem;
  /* max-width: 75ch; */
}
.uvodni-text{
  font-size: large;
  font-style: italic;
  margin-bottom: 3rem;
}
ul{
  padding-left:0 ;
}
.container{
  margin-bottom: 1rem;
  border-top: 0.2rem solid black;
  /* border-top: 0.2rem solid rgb(0, 253, 164); */
}
h1{
  color: rgb(0, 0, 0);
  font-size:x-large;
}
p{
  /* font-family: Arial, Helvetica, sans-serif; */
  font-family: 'Roboto', sans-serif;
  font-size: large;
  color: rgb(50, 50, 50);
  line-height: 1.2;
}
</style>
