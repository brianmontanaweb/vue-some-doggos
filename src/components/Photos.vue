<template>
    <div class="photo__container">
        <div class="photo__content"
             v-for="(photo, index) in photos"
             v-bind:style="{backgroundImage: 'url(http://fillmurray.com/200/200)'}"
             v-bind:key="index">
            <button>Save</button>
            <button>Remove</button>
        </div>
    </div>
</template>

<script lang="ts">
    import { Component, Vue } from 'vue-property-decorator';

    @Component({
        data() {
            return {
                photos: [1, 2, 3]
            }
        }
    })
    export default class Photos extends Vue {
    }
</script>