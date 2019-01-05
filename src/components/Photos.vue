<template>
    <div class="photo__container">
        <div class="photo__content"
             v-for="(photo, index) in photos"
             v-bind:style="{backgroundImage: `url(${photo})`}"
             v-bind:key="index">
            <button>Save</button>
            <button>Remove</button>
        </div>
    </div>
</template>

<script lang="ts">
    import { Component, Vue } from 'vue-property-decorator';

    @Component({
        props: ['photos']
    })
    export default class Photos extends Vue {
    }
</script>