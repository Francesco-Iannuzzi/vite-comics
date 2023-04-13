<!-- Descrizione:

Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
Quando la struttura a macroblocchi è pronta, popolate le voci di menu dinamicamente usando i data del componente.
Per oggi diamo priorità alla struttura: quando è tutto bello solido, passiamo al Sass!

Bonus:
Creare un componente aggiuntivo per gestire la fascia azzurra con le icone.

Consigli:
- iniziate a pensare prima alla struttura tutta dentro al componente pricipale App.vue. In un secondo momento fate refactoring creando componenti.
- Idem per il sass. Iniziate a scrivere tutto dentro app.scss o direttamente nei componenti singoli e poi fate refactoring creando parziali come visto in classe.
- Non dimenticate di analizzare il layout con Penpot -->

<script>
import SiteHeader from "./components/SiteHeader.vue";
import SiteMain from "./components/SiteMain.vue";
export default {
  components: {
    SiteHeader,
    SiteMain
  },
  data() {
    return {
    }
  }
}
</script>

<template>
  <SiteHeader></SiteHeader>
  <SiteMain></SiteMain>
  <footer></footer>
</template>

<style lang="scss">
@use '/node_modules/bootstrap/scss/bootstrap.scss';

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

header {
  padding: 1rem 0;

  .logo img {
    width: 3rem;
  }

  .navbar-nav a {
    font-size: 0.8rem;
    color: black;
  }
}

main {
  .content {
    background-color: black;
    color: white;
    display: flex;

    h1 {
      padding: 3rem 0;
      font-size: 2rem;
    }
  }

  .merch {
    background-color: blue;

    img {
      width: 2rem;
      object-fit: contain;
    }

    h2 {
      color: white;
      font-size: 0.75rem;
    }
  }
}
</style>