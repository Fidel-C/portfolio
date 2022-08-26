<template>
  <section class="container">
    <p class="subtitle has-text-centered is-4 is-italic p-4 has-text-light">
     {{service.details}}</p>

      <div v-if="service.title=='Projects'"  class="mx-auto">

      <div class="list">
       <div class="list-item" v-for="project in service.projects" :key="project.url">
           <a :href="project.url" target="_blank" class="has-text-centered has-text-warning">{{project.desc}}</a>
       </div>
      </div>



      </div>
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

