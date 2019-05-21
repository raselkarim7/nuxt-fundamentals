<template>
  <section class="container border">
    <div>
      <h1 >Vue-school-nuxt-fundamentals</h1>
      <h2 >My Awesome Nuxt.js Project.</h2>
      <div class="links p-2">
        <nuxt-link
          v-for="post in posts" 
          :key="post.id"
          :to="{name:'posts-id', params: {id: post.id}}"
          class="button-grey"
        >
          <span class="border rounded p-2 mx-2"> {{ post.title }} </span>
          
        </nuxt-link>
      </div>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  computed: {
    posts() {
      return this.$store.state.posts.all;
    }
  }
}
</script>

<style>

</style>
