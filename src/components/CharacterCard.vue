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
        padding: 2rem;
    }

    select{
        padding: .2rem 2rem .2rem 2rem;
        background-color: rgb(255, 119, 0);
        border-radius: none;
        border-style: none;
        margin-bottom: 70px;
    }
</style>