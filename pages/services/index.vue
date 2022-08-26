<template>
  <section class="container is-justify-content-center">
    <p class="subtitle is-4 is-italic p-4 has-text-light">
     {{service.details}}
    </p>
  </section>
</template>

<script>
export default {
props:{
  service:{
    type:Object,
    required:false
  }
}

}
</script>

