<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <div class="screen-size"></div>
  </header>

  <body>
    <div class="container">
      <div class="grid pokeball-img-wrapper">
        <img class="pokeball-home-img" src="https://cdn.pixabay.com/photo/2016/07/23/13/18/pokemon-1536849_960_720.png"
          alt="pokeball">
      </div>

      <div class="grid search-bar">
        <input class="item-search-bar" type="text" />
        <button class="item-button" type="button">Search</button>
      </div>
      <div class="grid below-search-bar">
        <select name="typeFilter1" id="typeFilter1">
          <option value="grass">Grass</option>
          <option value="water">Water</option>
          <option value="fire">Fire</option>
          <option value="electric">Electric</option>
        </select>
        <select name="typeFilter2" id="typeFilter2">
          <option value="grass">Grass</option>
          <option value="water">Water</option>
          <option value="fire">Fire</option>
          <option value="electric">Electric</option>
        </select>
        <button class="item-button" type="button">Poké Search Random</button>
      </div>
    </div>
  </body>
</template>

<style scoped lang="scss">
.grid {
  display: grid;
}

.container {
  margin: 0 auto;
}

.pokeball-img-wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 200px;
  margin-bottom: 30px;
}

.pokeball-home-img {
  max-width: 250px;
  max-height: 250px;
}

.search-bar {
  display: grid;
  grid-template-columns: 98.5% [start] 1.5% [break1];
}
.below-search-bar {
  display: grid;
  grid-template-columns: 15% [start] 15% [again] 70% [end];
}
.item-search-bar {
  width: 100%;
}
.item-button {
  justify-self: end;
  width: auto;
}

/* Media queries */
$breakpoint-phone: 576px;
$breakpoint-tablet: 768px;
$breakpoint-laptop: 992px;
$breakpoint-desktop: 1200px;

.screen-size {
  position: fixed;
  top: 0;
  left: 0;

  width: 100vw;
  height: 4px;
  background-color: blue;

  @media (min-width: $breakpoint-phone) {
    background-color: red;
  }

  @media (min-width: $breakpoint-tablet) {
    background-color: purple;
  }

  @media (min-width: $breakpoint-laptop) {
    background-color: lime;
  }

  @media (min-width: $breakpoint-desktop) {
    background-color: deeppink;
  }
}
</style>
