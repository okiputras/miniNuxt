<template>
  <section>
    <div>
      <adminPost :postid="editPost" />
    </div>
  </section>
</template>

<script>
import adminPost from '~/components/admin-post.vue'
export default {
  components: {
    adminPost
  },
  data() {
    return {
      editPost: {
        nama: 'oki',
        alamat: 'sananlove'
      }
    }
  },
  methods: {}
}
</script>
