<template>
  <section class="container">
    <div>
      <Head />
      <paper id="1" nama="oki putra" alamat="jalan sanan" />
      <logo />
      <h1 class="title">
        nuxtku
      </h1>
      <h2 class="subtitle">
        My prime Nuxt.js project
      </h2>
      <div class="links">
        <nuxt-link to="/blog">
          ohaiyo
        </nuxt-link>
        <input v-model="bid" type="text">
        <button @click="onClickPost">
          load blog
        </button>
        <nuxt-child />
      </div>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Head from '~/components/Head.vue'
import paper from '~/components/paper.vue'

export default {
  components: {
    Logo,
    Head,
    paper
  },
  data() {
    return {
      bid: ''
    }
  },
  methods: {
    onClickPost() {
      this.$router.push('/blog/' + this.bid)
    }
  },
  layout: 'blogs'
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
