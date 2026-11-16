---
title: Gallery
layout: base.njk
---
<style>
  .filters button.on {
    font-weight: bold;
    text-decoration: underline;
  }

  .topic img {
    max-width: 14rem;
    margin: 0.5rem;
  }
</style>
<script type="module" src="../js/is-land.js"></script>

<is-land on:visible>
<div id="gallery" v-scope="{ active: 'all' }">
  <div class="filters">
    <button @click="active = 'all'" :class="{ on: active === 'all' }" :aria-pressed="active === 'all'">All</button>
    <button @click="active = 'tech'" :class="{ on: active === 'tech' }" :aria-pressed="active === 'tech'">Tech</button>
    <button @click="active = 'media'" :class="{ on: active === 'media' }" :aria-pressed="active === 'media'">Media</button>
    <button @click="active = 'stores'" :class="{ on: active === 'stores' }" :aria-pressed="active === 'stores'">Stores</button>
  </div>
  <section class="topic" v-show="active === 'all' || active === 'tech'">
    <h3>Tech</h3>
    <img src="../img/tech/cdplayer.jpg" alt="Silver and black vertical CD player stereo system">
    <img src="../img/tech/dvdburner.jpg" alt="External silver DVD burner drive standing upright">
  </section>
  <section class="topic" v-show="active === 'all' || active === 'media'">
    <h3>Media</h3>
    <img src="../img/media/cds.jpg" alt="Tall stack of CD jewel cases on a stand">
    <img src="../img/media/shelf.jpg" alt="Wooden bookcase filled with physical media and collectibles">
  </section>
  <section class="topic" v-show="active === 'all' || active === 'stores'">
    <h3>Stores</h3>
    <img src="../img/stores/exchange.jpg" alt="Storefront of The Exchange entertainment shop">
    <img src="../img/stores/vincent.jpg" alt="Exterior storefront of St. Vincent de Paul thrift store">
  </section>
</div>
<template data-island>
  <script type="module">
    import { createApp } from '../js/petite-vue.js'
    createApp().mount('#gallery')
  </script>
</template>
</is-land>
