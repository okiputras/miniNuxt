<template>
  <section>
    <h1>
      {{ id }}
    </h1>
    <h2>
      {{ nama }}
    </h2>
    <h3>
      {{ alamat }}
    </h3>
  </section>
</template>
<script>
export default {
  props: {
    id: {
      type: String,
      required: true
    },
    nama: {
      type: String,
      required: true
    },
    alamat: {
      type: String,
      required: true
    }
  }
}
</script>
