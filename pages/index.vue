<template>
  <div>
    <b-container>
      <b-row>
        <b-col cols="0" md="2" />  
        <b-col cols="12" md="8">
          <b-container>
            <h4 style="margin-top:30%; margin-bottom:0px">
              Sales
            </h4>
            <h1 style="margin-top:0px; margin-bottom:10%">
              Gudang Ada
            </h1>
          </b-container>
          <b-form v-if="show" @submit="onSubmit" @reset="onReset">
            <b-form-group>
              <b-form-input
                id="exampleInput1"
                v-model="form.email"
                type="text"
                required
                placeholder="Masukan no Handphone"
              />
            </b-form-group>
            <b-form-group>
              <b-form-input
                id="exampleInput2"
                v-model="form.name"
                type="password"
                required
                placeholder="pin"
              />
            </b-form-group>
            <nuxt-link to="/dashboard">
              <b-button type="submit" class="btn-block" variant="danger">
                Login
              </b-button>
            </nuxt-link>  
            <!-- <b-button type="reset" class="btn-block" variant="danger">
              Reset
            </b-button> -->
          </b-form>
        </b-col>
        <b-col cols="0" md="2" />  
      </b-row>
    </b-container>

    <!-- b-col-7.vue -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        email: '',
        name: ''
      },
      show: true
    }
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault()
      alert(JSON.stringify(this.form))
    },
    onReset(evt) {
      evt.preventDefault()
      /* Reset our form values */
      this.form.email = ''
      this.form.name = ''
      /* Trick to reset/clear native browser form validation state */
      this.show = false
      this.$nextTick(() => {
        this.show = true
      })
    }
  }
}
</script>

<!-- b-form-1.vue -->
