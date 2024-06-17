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
        getCharacters(){
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
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
            console.log('ciao');

        }    
    
        
    }

    
        
}

</script>

<template>
    
    <CharactersList :Characters="characters"/>

</template>

<style>
</style>