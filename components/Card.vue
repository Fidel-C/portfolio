<template>
    <div class="card">
      <header class="card-header">
        <p class="card-header-title has-text-grey has-text-centered">
          {{ title }}
        </p>
      </header>
      <div class="card-content is-justify-content-center">
        <div class="card-image">
          <figure :class="`image is-${ratio}`">
              <img :src="src">
          </figure>

        </div>
      <footer class="card-footer is-justify-content-center p-1">
        <div class="card-footer-item">

          <slot name="footer" />

        </div>
      </footer>
      </div>
    </div>


 </template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: false
    },
    icon: {
      type: String,
      required: false
    },
    ratio:{
      type:String,
      required:false
    },
    src:{
      type:String,
      required:false

    },

  }
}
</script>
