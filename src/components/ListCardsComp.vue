<script>

    import CardComp from './CardComp.vue';
    import axios from 'axios'
    import {store} from '../store'

    export default{

        name: "ListCardsComp",
        
        components:{
            CardComp
        },

        data(){
            return{

                NCards: 0,
                store

            }
        },

        created(){
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=102&offset=3')
            .then(response => {
                this.store.cards = response.data.data;
                console.log(this.store.cards);
                console.log(this.store.cards[0].name);
                console.log(this.store.cards[0].type);
                this.NCards = this.store.cards.length
        
            })
        },

        methods:{
    

        },
    }
    
</script>




<template>
    <div id="ListCardsComp">

        <div id="TopBar">
            <p>Found {{ NCards }} cards</p>
        </div>

        <div id="CardContainer" class="col-12">
            <CardComp  
            v-for="(item, index) in store.cards" :key="index"
            :image="store.cards[index].card_images[0].image_url"
            :name="store.cards[index].name"
            :type="store.cards[index].type"
             id="card" class="col-2"/>

            <!-- <CardComp v-for="(item, index) in cards" :key="index"
           :image="cards[index].card_images[0].image_url"
            :name="cards[index].name"
            :type="cards[index].type"
            /> -->
        </div>

    </div>
</template>





<style lang="scss" scoped>


#ListCardsComp {

    color: white;
    width: 80rem;
    background-color: white;
    padding: 1rem;


    #TopBar {
        background-color: black;
        line-height: 2.5rem;
        text-indent: 1rem;
    }

    #CardContainer {
        width: 100%;
        color: rgb(255, 255, 255);
        display: flex;
        flex-wrap: wrap;

        #card {
            display: flex;
            flex-direction: column;
            align-items: center;
            border: solid rgb(119, 119, 119) 1px;
            padding: 0.8rem;
            background-color:#d48e38;
            text-align: center;
        }
    }

}

</style>