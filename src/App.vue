<script>
import AppMain from './components/AppMain.vue';
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';

export default{
    components:{
        AppMain,
        AppFooter,
        AppHeader,
    },
    data(){
        return{

        }
    }
}

</script>

<template>
    <AppMain/>
    <AppHeader/>
    <AppFooter/>

</template>

<style lang="scss">
@use '../style/general.scss';
@use '../node_modules/bootstrap/scss/bootstrap.scss';
</style>
