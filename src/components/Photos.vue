<template>
    <div class="photo__container">
        <div class="photo__content" v-bind:style="{backgroundImage: 'url(http://fillmurray.com/200/200)'}">
            <button>Save</button>
            <button>Remove</button>
        </div>
    </div>
</template>

<script lang="ts">
    import { Component, Vue } from 'vue-property-decorator';

    @Component
    export default class Photos extends Vue {
        
    }
</script>