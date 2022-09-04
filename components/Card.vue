<template>
    <div class="card is-justify-content-center is-align-items-center p-1">
      <header class="card-header mx-auto">
        <p class="has-text-light has-text-centered mx-auto">
          {{ title }}
        </p>
      </header>
      <div class="card-content has-text-weight-bold is-justify-content-center">
        <div class="card-image">
          <figure :class="`image is-${ratio}`">
              <img :src="src">
          </figure>

        </div>

      <div class="card-footer is-justify-content-center mx-auto">
        <div class="card-footer-item">

          <slot name="footer" />

        </div>
      </div>

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

<style>
.card{
  background-image: linear-gradient(rgb(47, 3, 47),black);
  color:white;
}
</style>
