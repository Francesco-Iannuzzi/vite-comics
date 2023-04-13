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
import SiteFooter from "./components/SiteFooter.vue";
export default {
  components: {
    SiteHeader,
    SiteMain,
    SiteFooter,
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
  <SiteFooter></SiteFooter>
</template>

<style lang="scss">
@use '/node_modules/bootstrap/scss/bootstrap.scss';
@use './assets/scss/partials/variables' as *;

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
    color: $darker;

    &:hover {
      color: $dc_color;
    }
  }
}

main {
  .content {
    background-color: $darker;
    color: $light;
    display: flex;

    h1 {
      padding: 3rem 0;
      font-size: 2rem;
    }
  }

  .merch {
    background-color: $dc_color;

    img {
      width: 2rem;
      object-fit: contain;
    }

    h3 {
      color: $light;
      font-size: 0.75rem;
    }
  }
}

footer {
  .up_footer {
    background-image: url(./assets/img/footer-bg.jpg);
    height: 20rem;

    .footer_left {
      color: $light;

      h2 {
        font-size: 1rem;
      }

      ul {
        list-style: none;
        padding: 0;
        font-size: 0.7rem;

        a {
          text-decoration: none;
          color: $icon;
        }
      }
    }

    .footer_right {

      img {
        height: 20rem;
        align-self: center;
      }
    }
  }

  .bottom_footer {
    background-color: $dark;
    z-index: 1;

    .sign {
      h2 {
        font-size: 1rem;
        color: $light;
        padding: 0.5rem;
        border: 2px solid $dc_color;
      }

    }

    .social {
      h2 {
        font-size: 1rem;
        color: $dc_color;
      }

      ul {
        list-style: none;
        color: $icon;
      }
    }
  }
}
</style>