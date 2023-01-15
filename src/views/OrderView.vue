<template>
    <div class="order-page">

      <section class="section-text">
        <p>Momentálně příjmáme objednávky prostřednictvím emailiu. Napiš nám na adresu
          <a href="mailto:trika.bias@gmail.com"> trika.bias@gmail.com </a> jaký motiv a jakou barvu trička chceš (aktuálně nabízíme bílou, šedou a černou) a my na tom začnem pracovat. Taky nám nezapomeň napsat adresu, triko ti na ní zašleme dobírkou.</p>
        <!-- <p>Nebo nás kontaktuj prostřednictvím formuláře níže.</p> -->
      </section>

      <!-- <form class="contact-form" action="">
        <input 
          type="text" 
          name="name" 
          placeholder="Jméno">
        <input 
          type="email" 
          name="email" 
          placeholder="Váš email" 
          required>
        <textarea 
          name="message" 
          id="message" 
          placeholder="Zpráva" 
          cols="30" rows="10">
        </textarea>
        <button type="submit">Odeslat</button>
      </form> -->

    </div>
</template>

<script>
export default{
  data() {
    return {
      submited: false,
    }
  },
}
</script> 

<style scoped>
  .order-page{
    max-width: 900px;
    margin: 0 auto;
    padding: 0rem 3rem;
    /* max-width: 75ch; */
  }
  .section-text{
    margin-bottom: 3rem;
    font-size: large;
    font-style: italic;
  }
  .contact-form{
    display: flex;
    flex-direction: column;
    gap: .5rem;

    max-width:600px;
    margin: 0 auto;

    border-top: solid black .2rem;
    padding-top:3rem ;
  }
  .contact-form input{
    height: 2rem;
    border: solid black .1rem;
    background-color: none;

    font-family: 'Roboto', sans-serif;
    font-size: medium;
  }
  .contact-form textarea{
    border: solid black .1rem;
    background-color: none;

    font-family: 'Roboto', sans-serif;
    font-size: medium;
  }
  .contact-form button{
    height: 2rem;
    width: 10ch;
    background-color: rgb(175, 175, 175);
    border: none;
    /* box-shadow: .2rem .2rem .3rem rgba(0, 0, 0, 0.1); */

    font-family: 'Unbounded', 'Courier New', Courier, monospace;
    font-size: medium;
  }
  .contact-form button:hover{
    background-color: var(--green-color);
    cursor: pointer;
  }
</style>