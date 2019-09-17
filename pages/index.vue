<!--<template>-->
<!--  <div class="container">-->
<!--    <p>Hello {{ name }}!</p>-->
<!--    <nuxt-link to="/about">-->
<!--      Go to /about-->
<!--    </nuxt-link>-->
<!--  </div>-->
<!--</template>-->

<!--<script>-->
<!--export default {-->
<!--  asyncData () {-->
<!--    return new Promise((resolve) => { // eslint-disable-next-line nuxt/no-timing-in-fetch-data-->
<!--      setTimeout(function () {-->
<!--        resolve({ name: 'world' })-->
<!--      }, 1000)-->
<!--    })-->
<!--  }-->
<!--}-->
<!--</script>-->

<!--<style scoped>-->
<!--  .container {-->
<!--    font-size: 20px;-->
<!--    text-align: center;-->
<!--    padding-top: 100px;-->
<!--  }-->
<!--</style>-->

<template>
  <div class="container">
    <h2>Users</h2>
    <ul class="users">
      <li v-for="user in users" :key="user.id">
        <NuxtLink :to="'/users/'+user.id">
          {{ user.name }}
        </NuxtLink>
      </li>
    </ul>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  async asyncData () {
    const { data } = await axios.get('https://jsonplaceholder.typicode.com/users')
    return { users: data }
  }
}
</script>

<style scoped>
  .container {
    text-align: center;
    margin-top: 100px;
    font-family: sans-serif;
  }
  .users {
    list-style-type: none;
  }
  .users li a {
    display: inline-block;
    width: 200px;
    border: 1px #ddd solid;
    padding: 10px;
    text-align: left;
    color: #222;
    text-decoration: none;
  }
  .users li a:hover {
    color: orange;
  }
</style>
