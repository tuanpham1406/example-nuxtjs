<!--CUSTOM LOADING PAGE-->

<!--<template>-->
<!--  <div class="container">-->
<!--    <p>About Page</p>-->
<!--    <p>It should take 5 seconds for the loader to disappear</p>-->
<!--    <p>-->
<!--      It should take 5 seconds for the route to change after you-->
<!--      <span class="link" @click="goToFinal">-->
<!--        click here-->
<!--      </span>-->
<!--    </p>-->
<!--  </div>-->
<!--</template>-->

<!--<script>-->
<!--export default {-->
<!--  loading: false,-->
<!--  asyncData () {-->
<!--    return new Promise((resolve) => { // eslint-disable-next-line nuxt/no-timing-in-fetch-data-->
<!--      setTimeout(function () {-->
<!--        resolve({})-->
<!--      }, 1000)-->
<!--    })-->
<!--  },-->
<!--  mounted () {-->
<!--    setTimeout(() => {-->
<!--      // Extend loader for an additional 5s-->
<!--      this.$nuxt.$loading.finish()-->
<!--    }, 5000)-->
<!--  },-->
<!--  methods: {-->
<!--    goToFinal () {-->
<!--      // Start loader immediately-->
<!--      this.$nuxt.$loading.start()-->
<!--      // Actually change route 5s later-->
<!--      setTimeout(() => {-->
<!--        this.$router.push('/final')-->
<!--      }, 5000)-->
<!--    }-->
<!--  }-->
<!--}-->
<!--</script>-->

<!--<style scoped>-->
<!--.link {-->
<!--  cursor: pointer;-->
<!--  text-decoration: underline;-->
<!--}-->
<!--.container {-->
<!--  font-size: 20px;-->
<!--  text-align: center;-->
<!--  padding-top: 100px;-->
<!--}-->
<!--</style>-->

<template>
  <div class="content">
    <h1 class="title">
      Another page
    </h1>
    <p><nuxt-link to="/" class="button is-medium is-primary hvr-float-shadow">Another button</nuxt-link></p>
    <p><nuxt-link to="/">Back home</nuxt-link></p>
  </div>
</template>
