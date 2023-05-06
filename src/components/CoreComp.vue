<script>
    import ListCardsComp from './ListCardsComp.vue';

    export default{

        name: "CoreComp",
        
        components: {
           ListCardsComp
        },

        data(){
            return{
               


            }
        },
        methods: {


        },
    }
    
</script>




<template>
    <div id="CoreComp">
        <ListCardsComp/>
    </div>
</template>





<style lang="scss" scoped>


#CoreComp {

    color: white;
    background-color: #d48f38;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 3rem 0rem;
}

</style>