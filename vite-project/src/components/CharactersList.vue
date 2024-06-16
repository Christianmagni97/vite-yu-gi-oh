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
<section class="characters-list container">
    <div class="row">
        <h1 class="col-12">
            Yu Gi Oh cards
        </h1>
        <div class="col-12">
            <div class="row">
                <article v-for="character in characters" :key="character.id" class="col-3">
                <div class="card w-100" ;>
                   <img :src="character.img" class="card-img-top" alt="...">
                   <div class="card-body">
                      <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                   </div>
                </div>
                {{ character.name }}
            </article>

            </div>
            
        </div>
    </div>
</section>

</template>

<style>
</style>