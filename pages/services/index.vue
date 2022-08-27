<template>
  <section class="container">
    <p class="is-subtitle  is-bold has-text-centered is-italic p-4 has-text-light" :class="service.title=='Projects Showcase'? 'is-size-3 is-underlined has-text-weight-bold':'is-size-4'">
     {{service.details}}</p>

      <div v-if="service.title=='Projects Showcase'"  class="mx-auto">

      <div class="menu-list is-hoverable">
        <ol>
          <div class="list-item my-2">
          <li v-for="project in service.projects" :key="project.url">
           <a :href="project.url" target="_blank" class="is-italic has-text-warning">{{project.desc}}</a>
          </li>
       </div>
        </ol>
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

