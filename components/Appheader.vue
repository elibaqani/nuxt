<template>
  <div> 
      <h1>header</h1>
      <ul>
          <li><nuxt-link to="/">home page</nuxt-link></li>
          <li><nuxt-link to="about">about page</nuxt-link></li>
          <li><nuxt-link to="jokes">dad jokes</nuxt-link></li>
      </ul>
  </div>
</template>

<script>
export default {
    name:'Appheader'
}
</script>
