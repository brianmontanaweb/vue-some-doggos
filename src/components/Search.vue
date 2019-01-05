<template>
    <form class="search-form">
        <label for="search500px" class="search-form__label">Let's look at dog breeds</label>
        <select
            id="search500px"
            placeholder="Search"
            class="search-form__input">
            <option value="1">Dog 1</option>
        </select>
    </form>
</template>

<script lang="ts">
    import { Component, Vue } from 'vue-property-decorator';

    @Component
    export default class Search extends Vue {
        
    }
</script>