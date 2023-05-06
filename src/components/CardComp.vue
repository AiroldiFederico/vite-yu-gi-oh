<script>


    export default{

        name: "CardComp",

        props: {

            name: String,
            type: String,
            image: String,
        },
        
        components:{

        },

        data(){
            return{
               
                cards: []

            }
        },


        methods:{
    

        },
    }
    
</script>




<template>
    <div id="CardComp">
     
        <img :src="image" alt="">

        <span>{{name}}</span>

        <span style="color:black">{{type}}</span>

    </div>
</template>





<style lang="scss" scoped>

    span {
        font-size: 1rem;
        margin: 1rem 0rem;
    }

    img {
        max-width: 100%;
        max-height: 100%;
    }


</style>