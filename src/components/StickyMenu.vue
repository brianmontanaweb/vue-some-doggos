<template>
    <div class="sticky-menu">
        <h1 class="sticky-menu__logo">Logo</h1>
        <span class="sticky-menu__toggle">Menu</span>
        <ul class="sticky-menu__list">
          <li>
            <a href="#favorites"
               class="sticky-menu__link">Favorites</a>
          </li>
        </ul>
      </div>
</template>

<script lang="ts">
  import { Component, Vue } from 'vue-property-decorator';

  @Component
  export default class StickyMenu extends Vue {
      
  }
</script>
