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
    background-color: rgb(218, 197, 37);
    width: 100%;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

</style>