<script>
import { store } from '../store';
import CharactersList from'../components/CharactersList.vue';
import AppSearch from './AppSearch.vue';
import axios from 'axios';

export default {
    data() {
        return {
            store,
            characters:[]
        };
    },
    components: {
        AppSearch ,
        CharactersList,

    },
    methods:{
        getCharacters{
            axios.get('https://rickandmortyapi.com/api/character')
            .then(function (response) {
    
                console.log(response);
            })
            .catch(function (error) {
   
                console.log(error);
            })
            .finally(function () {
            });
        },
        created(){
            this.getCharacters();

        }    
    
        
    }

    
        
}

</script>

<template>
    
    <CharactersList/>

</template>

<style>
</style>