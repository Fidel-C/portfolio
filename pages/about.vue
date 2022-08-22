<template>
  <section class="section">

  <div class="is-rounded p-3" style="border-radius:30%">
        <h2 class="title is-5 has-text-light has-text-centered mb-2"> About the Author</h2>
    <section class="section " style="border-radius:50%">
      <h3 class="subtitle is-6 is-italic is-semibold has-text-warning has-text-centered">
    Hi, I am Fidel, a self-taught software developer, amongst other things.<br>
    I'm keen on, and experienced in both the frontend and
     the backend sides of software development, by which I can code modern, dynamic
     and interactive interfaces for your personal, business or social use. <br>
    You can always count on me for your web/mobile app related needs and more <span class="is-not-italic" >&#128521;</span>.
    <br> Please feel free to reach me on any one of the links on the <NuxtLink class="subtitle is-5 is-italic has-text-warning is-link" :to="{name:'contact'}">contact page</NuxtLink>.
    <br> Thanks a bunch.</h3>
    </section>
</div>
  </section>
</template>

<script>
export default {
 head(){
return{
  title:`Onqode | ${this.$route.name}`
}
  },

}
</script>

<style>

</style>
