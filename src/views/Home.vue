<template>
  <div class="home">
    <StickyMenu></StickyMenu>
    <Search></Search>
    <Photos></Photos>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import StickyMenu from '@/components/StickyMenu.vue';
import Search from '@/components/Search.vue';
import Photos from '@/components/Photos.vue';

@Component({
  components: {
    StickyMenu,
    Search,
    Photos
  },
})
export default class Home extends Vue {}
</script>
