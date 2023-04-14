<!-- Descrizione:

Milestone 1
Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
Quando la struttura a macroblocchi è pronta, popolate le voci di menu dinamicamente usando i data del componente.
Per oggi diamo priorità alla struttura: quando è tutto bello solido, passiamo al Sass!

Bonus:
Creare un componente aggiuntivo per gestire la fascia azzurra con le icone.

Milestone 2
Continuate a lavorare nella stessa repo di ieri e create un nuovo componente che rappresenterà le card dei fumetti.
Utilizzate i dati presenti nel file json che trovate in allegato e passateli al componente Card tramite props.
Una volta inseriti tutti i contenuti dinamicamente, completate il vostro layout e rifinite i dettagli con Sass. -->

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
</style>