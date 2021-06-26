<template>
  <div >
    <Joke v-for="joke in jokes" 
    :key="joke.id"
    :id="joke.id"
    :joke="joke.joke"
    />
  </div>
</template>

<script>
import axiox from 'axios'
import Joke from '~/components/Joke.vue'

export default {
  components:{
    Joke 
    },
    async asyncData(){
       const config = {
              headers:{
                Accept:"application/json"
              }
       }
         let res = await axiox.get('https://icanhazdadjoke.com/search',config);
         return {jokes :  res.data.results}

    },
  
    head(){
        return{
            title:'jokes page',
            meta:[
                {
                hid:'description',
                name:'description',
                content:'jokes'
                }
            ]
        }
    }
}
</script>