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
            .then((response) =>{
    
                console.log(response.data.results);
                this.characters = response.data.results;
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
    
    <CharactersList :characters="characters"/>

</template>

<style>
</style>