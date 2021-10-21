<template>
    <div class="basic-layout">
        <Menu/>
        <div class="ui ">
            <slot/>
        </div>
        <Footer/>

    </div>
</template>

<script>
import Footer from '../components/Footer.vue';
import Menu from '../components/Menu.vue';
export default {
    name: 'BasicLayouts',
    components: {
        Menu,
        Footer 
    },
};
</script>

<style>

</style>