<script>

    import SelectComp from './SelectComp.vue';
    import {store} from '../store'

    export default{

        name: "SelectsComp",

        data(){
            return{

                store

            }
        },

        created(){

        },

        methods:{
    

        },
    }
    
</script>




<template>
    <div id="SelectComp">
        <!-- <select class="form-select" aria-label="Default select example">
            <option selected>Open this select menu</option>
            <option value="1">One</option>
            <option value="2">Two</option>
            <option value="3">Three</option>
        </select> -->

        <select class="form-select" aria-label="Default select" v-model="store.selected">
            <option selected>Open this select menu</option>
            <option v-for="(archetype, index) in this.store.archetypes" :key="index" :value="archetype">{{ archetype }}</option>
        </select>
    </div>
</template>





<style lang="scss" scoped>

    select {
        line-height: 1;
    }

</style>