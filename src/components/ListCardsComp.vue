<script>

    export default{

        name: "ListCardsComp",
        
        components: {
            
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
    <div id="ListCardsComp">

        <div id="TopBar">
            <p>Found n/ cards</p>
        </div>

        <div id="CardContainer">

        </div>

    </div>
</template>





<style lang="scss" scoped>


#ListCardsComp {

    color: white;
    width: 80rem;
    //height: 40rem;
    background-color: white;
    padding: 1rem;

    #TopBar {
        background-color: black;
        line-height: 2.5rem;
        text-indent: 1rem;
    }

    #CardContainer {
        background-color: rgb(212, 255, 255);
        width: 100%;
        height: 40rem;
    }

}

</style>