<template>
    <div>
        {{ joke }}
    </div>
</template>

<script>

import axiox from 'axios'
export default {
   async asyncData ({params}) {
         const config = {
              headers:{
                Accept:"application/json"
              }
       }
         let res = await axiox.get(`https://icanhazdadjoke.com/j/${ params.id }`,config);
         return {joke :  res.data.joke}

    },
        head(){
        return{
            title:'Joke',
            meta:[
                {
                hid:'description',
                name:'description',
                content: this.joke
                }
            ]
        }
    }
}
</script>