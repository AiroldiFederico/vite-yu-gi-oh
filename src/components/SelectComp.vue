<script>

    import SelectComp from './SelectComp.vue';
    import {store} from '../store'

    export default{

        name: "SelectsComp",

        data(){
            return{

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
        <select class="form-select" aria-label="Default select example">
            <option selected>Open this select menu</option>
            <option value="1">One</option>
            <option value="2">Two</option>
            <option value="3">Three</option>
        </select>
    </div>
</template>





<style lang="scss" scoped>

    select {
        line-height: 1;
    }

</style>