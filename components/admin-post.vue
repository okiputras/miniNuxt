<template>
  <section>
    aw
    <logo />
    <b-alert show>
      Default Alert
    </b-alert>
    <div>
      <appController
        v-model="editPost.nama"
      >
        Name
      </appController>
      <appController
        v-model="editPost.alamat"
      >
        alamat
      </appController>
      <appButton
        style="margin-left: 10px"
        @click="onSave"
      >
        save
      </appButton>
      <appButton
        style="margin-left: 10px"
        @click="onCancel"
      >
        cancel
      </appButton>
    </div>
  </section>
</template>
<script>
import Logo from '~/components/Logo.vue'
import appController from '~/components/appController.vue'
import appButton from '~/components/appButton.vue'
export default {
  components: {
    Logo,
    appButton,
    appController
  },
  props: {
    postid: {
      type: Object,
      required: false,
      default: Object
    }
  },
  data() {
    return {
      editPost: this.editPost
        ? { ...this.editPost }
        : {
            nama: 'a',
            alamat: 'b'
          }
    }
  },
  methods: {
    onCancel() {
      this.$router.push('/')
    },
    onSave() {
      this.$router.push('/about')
    }
  }
}
</script>
