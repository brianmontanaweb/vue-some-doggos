<template>
  <div class="home">
    <StickyMenu></StickyMenu>
    <Search :getSelectedBreed="getSelectedBreed"></Search>
    <Photos :photos="photos"></Photos>
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
    Photos,
  },
  data() {
    return {
      photos: []
    }
  },
  methods: {
    getSelectedBreed: function(e) {
      fetch(`https://dog.ceo/api/breed/${e.target.value}/images`)
        .then(res => res.json())
        .then(resJson => {
          this.$data.photos = resJson.message;
        })
    }
  }
})
export default class Home extends Vue {
  
}
</script>
