<template>
  <div >

  <div class="is-rounded mx-auto p-2 col-sm-10 col-md-8 col-lg-6 col-xl-6" style="border-radius:30%;  background-image: linear-gradient(rgb(47, 3, 47),black);box-shadow: darkslateblue;">
        <h2 class="title is-6 is-bold has-text-light has-text-centered mb-1 is-underlined"> About the Author</h2>
    <div class="p-3">
      <p class="subtitle is-bold is-6 is-italic is-semibold has-text-light has-text-centered">
    I am Fidel, a self-taught software developer.<br>
    I have many hobbies one of which is coding. I'm experienced in both the frontend and
     the backend sides of software development, by which I can code modern, dynamic
     and interactive interfaces for your personal, business or social use. <br>
    You can always count on me for your web/mobile app related needs and more <span class="is-not-italic" >&#128521;</span>.
    <br> Please feel free to reach me on any one of the links on the <NuxtLink class="subtitle is-5 is-italic has-text-warning is-link" :to="{name:'contact'}">contact page</NuxtLink>.
    <br> Thanks a bunch.</p>


  </div>
</div>

</div>
</template>

<script>
export default {
 head(){
return{
  title:`PrettyQode | ${this.$route.name}`
}
  },

}
</script>

<style>

</style>
