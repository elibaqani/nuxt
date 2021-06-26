<template>
  <div >
    <h1>this is my about page</h1>
  </div>
</template>

<script>
export default {
    head(){
        return{
            title:'about page',
            meta:[
                {
                hid:'description',
                name:'description',
                content:'this is my about page'
                }
            ]
        }
    }
}
</script>