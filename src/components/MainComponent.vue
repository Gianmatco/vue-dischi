<template>
<main>
    <div class="container-card">
        <div class="row">
        
        <div v-for="(album, index) in albumList" :key="index" class="col-lg-3 d-flex flex-wrap flex-lg-nowrap">
            <app-card :item="album"/>

        </div>
    
    </div>
    </div>
    
    
    
    
</main>
</template>

<script>
import axios from 'axios';
import AppCard from './AppCard.vue';

export default {
  
    name: 'MainComponent',
    components: { 
        AppCard, 
        },
    
    data(){
        return{
            albumList:[],
            apiPath:'https://flynn.boolean.careers/exercises/api/',
        }

    },
    mounted(){
        axios.get(this.apiPath + 'array/music').then((res)=>{
            console.log(res)
            this.albumList = res.data.response
            
        })
    }

    
}
</script>

<style lang="scss" >
main{
    background-color: #1e2d3b;
    
   
    color: white;

    .container-card{
        width: 60%;
        margin: 0 auto;



        .box-card{
            align-content: center;
            width: 200px;
        }
           
          
    }


    
    .card{
        color: black;
        flex: wrap;
    }
    
    
}

</style>