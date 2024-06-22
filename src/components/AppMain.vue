<script>
    import CharactersList from './CharactersList.vue';
    import CharactersCard from './CharacterCard.vue';
    import axios from 'axios';
    import { store } from '../store.js'

    export default {
        components:{
            CharactersCard,
            CharactersList,
        },
        
        data() {
    return {
        store,
        archetypes:[]
    }
},

methods:{
    // API
    getCharacters(){
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
        .then((response) => {
        console.log(response.data.data);
        this.store.caratteri = response.data.data
        })
        .catch(function (error) {
        console.log(error);
        });
        },
    
        getArchetypes(){
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
            .then((response) => {
            console.log(response.data.data);
            this.archetypes = response.data.data
            })
            .catch(function (error) {
            console.log(error);
            });
        },
    
    funzioneDiProva() {
        console.log('')
    }
},
created(){
    this.getCharacters();
    this.funzioneDiProva();
    this.getArchetypes();
}

}
</script>

<template>
    <main>
        <CharactersCard @cerca="funzioneDiProva" :archetypes="archetypes"/>
        <CharactersList :caratteri="store.caratteri"/>
        
    </main>
</template>

<style lang="scss" scoped>
    @use './style/partials/mixins.scss' as*;
    @use './style/partials/variabls.scss' as*;
</style>