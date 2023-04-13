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
export default {
  data() {
    return {
    }
  }
}
</script>

<template>
  <header>
    <div class="logo">
      <img src="../public/img/dc-logo.png" alt="">
    </div>
    <nav class="navbar navbar-expand-lg bg-light">
      <div class="container-fluid">
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <a class="nav-link" href="#">characters</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">comics</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">movies</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">tv</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">games</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">collectibles</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">videos</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">fans</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">news</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">shop</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </header>
  <main></main>
  <footer></footer>
</template>

<style lang="scss" scoped></style>