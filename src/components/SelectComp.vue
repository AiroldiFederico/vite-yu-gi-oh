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
        <select class="form-select" aria-label="Default select" v-model="store.selected" @change="$emit('nomeEmit')">
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