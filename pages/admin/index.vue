<template>
  <section>
    <h2 class="ikan">
      Admin Page
    </h2>
    <div class="ikan">
      <button @click="$router.push('admin/newPost')">
        create new post
      </button>
    </div>
    <hr>
    <div class="ikan">
      <h5>existing data</h5>
      <paper id="1" nama="oki putra" alamat="jalan sanan" />
      <paper id="2" nama="oki" alamat="sanan" />
    </div>
    <hr>
  </section>  
</template>

<script>
import paper from '~/components/paper'
export default {
  components: {
    paper
  }
}
</script>

<style scoped>
.ikan {
  text-align: center;
}
</style>
