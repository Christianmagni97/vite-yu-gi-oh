<script>
import CharactersCard from'./CharacterCard.vue';
export default{
    components:{
        CharacterCard,
    },
    data(){
        return{

        }
    },
    props:{
        Characters:{
            type: Array,
            required: true,

        }

    }
}


</script>


<template>
<CharacterCard/>
<ul>
    <li v-for="character in characters" :key="character.id">
        {{ character.name }}

    </li>
</ul>
</template>

<style>
</style>