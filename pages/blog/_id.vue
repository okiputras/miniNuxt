<template>
  <section>
    <h1>hai {{ $route.params.id }}</h1>
    <h2>omg</h2>
  </section>  
</template>

<script>
export default {
  validate(data) {
    return /^\d+$/.test(data.params.id)
  }
}
</script>
