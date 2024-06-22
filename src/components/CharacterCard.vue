<script>
    export default {
        data() {

        },
        props: {
            archetypes: Array
        }
}
</script>

<template>
    <label for="carta"><strong>Scegli la carta:</strong></label>
    <select @click="$emit('cerca')">
        <option value="0" v-for="item in archetypes" :key="item.id">
        {{ item.archetype }}
        </option>
    </select>
</template>

<style lang="scss" scoped>
    label {
        text-transform: uppercase;
        padding: 1rem;
    }

    select{
        padding: .3rem 1rem .3rem 1rem;
        background-color: rgb(255, 119, 0);
        border-radius: .5rem;
        border-style: none;
        margin-bottom: .5rem;
    }
</style>