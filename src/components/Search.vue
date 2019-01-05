<template>
    <form class="search-form">
        <label for="search500px" class="search-form__label">Let's look at dog breeds</label>
        <select
            id="search500px"
            placeholder="Search"
            class="search-form__input"
            v-on:change="getSelectedBreed($event)">
            <option v-for="(breed, index) in breeds"
                    :key="index"
                    :value="breed">{{breed}}</option>
        </select>
    </form>
</template>

<script lang="ts">
    import { Component, Vue } from 'vue-property-decorator';
                    
    @Component({
        props: ['getSelectedBreed'],
        data() {
            return {
                getBreeds: () => {
                    return fetch('https://dog.ceo/api/breeds/list/all')
                    .then(res => res.json())
                    .then(resJson => {
                        const breedsObj = resJson.message;
                        const breedsArr = Object.keys(breedsObj);
                        for (const key in breedsObj) {
                            if (breedsObj[key].length) {
                                breedsObj[key].map((el: string) => `${key}-${el}`).forEach((el: string) => breedsArr.push(el));
                            }
                        }
                        return breedsArr;
                    });
                },
                breeds: [],
                selectedBreed: ''
            }
        },
        created: function() {
            this.$data.getBreeds().then((res: string[]) => {
                this.$data.breeds = res;
            })
        }
    })
    export default class Search extends Vue {
        
    }
</script>