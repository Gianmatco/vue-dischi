<template>
<!-- author: "Bon Jovi"
            genre: "Rock"
            poster: "https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg"
            title: "New Jersey"
        year: "1988"-->
        
            <div class="card  mt-4 gy-5 text-center" >
                <img :src="item.poster"  >
                <h5 >{{item.title}}</h5>
                <p >{{item.author}}</p>
                <p>{{item.year}}</p>
            
            </div>
        

    
</template>


<script>
export default {
    name:'AppCard',
    props:{
        item: Object,
    }
    
}
</script>

<style lang="scss">


</style>