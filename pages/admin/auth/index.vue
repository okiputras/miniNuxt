<template>
  <section>
    <span style="text-align:center">
      Login
    </span>
    <b-alert show>
      Default Alert
    </b-alert>
    <div>
      <appController
        type="email"
      >
        Name
      </appController>
      <appController
        type="password"
      >
        password
      </appController>
      <appButton
        style="margin-left: 20px"
        type="submit" 
      >
        {{ isLogin ? "login" : "register" }}
      </appButton>
      <appButton
        style="margin-left: 20px"
        @click="isLogin = !isLogin" 
      >
        Switch to {{ isLogin ? "login" : "register" }}
      </appButton>
    </div>
  </section>
</template>
<script>
import appController from '~/components/appController.vue'
import appButton from '~/components/appButton.vue'
export default {
  components: {
    appButton,
    appController
  },
  data() {
    return {
      isLogin: false
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
