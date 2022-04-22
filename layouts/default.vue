<template>
  <div class="has-background-primary layout" style="min-height: 100vh;
    min-width: 100%;">
    <section class="section is-flex is-flex-direction-column is-justify-content-center is-align-items-center">
                      <h1 class="has-text-centered is-italic title is-4 has-text-warning has-text-weight-bold mt-3"> Onqode </h1>
      <h1
        class="has-text-centered is-italic title is-4 has-text-warning has-text-weight-bold mt-3"
      >
       "I Code and Design <span class="subtitle is-5 has-text-light is-italic is-underlined">beautiful and really simple things."</span>
      </h1>
    </section>
    <section class="section">
      <div class="columns">
        <aside class="column is-2 section">

          <ul class="menu-list is-flex-mobile">
            <li
              v-for="(item, key) of items"
              :key="key"
              class="has-text-weight-bold links"
            >
              <NuxtLink :to="item.to" exact-active-class="is-active">
                <b-icon :icon="item.icon" class="has-text-warning" />
                {{ item.title }}
              </NuxtLink>
            </li>
          </ul>
        </aside>

        <div class="container column is-10">
          <transition name="fade">
          <Nuxt />
          </transition>
        </div>
      </div>
    </section>
    <footer class="is-flex is-flex-direction-column footer has-background-warning-dark has-text-light is-italic is-justify-content-center is-align-items-center">
            <div class="is-justify-content-center mb-5"  style="width:100px">
         <b-image
       src="/logoDark.png"
       ratio="16by9" 
       :responsive="responsive"
       is-rounded
       >

       </b-image>
      </div>
      
      <p class="has-text-centered has-text-weight-semi-bold is-size-5">
        
        Coded & Designed by
        <span class="has-text-warning has-text-weight-bold">Fidel C. </span>
        &copy <p class="has-text-warning has-text-weight-bold"> Onqode {{ new Date().getFullYear() }}
      </p>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      responsive:true,
      items: [
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' },
        },
        {
          title: 'Services',
          icon: 'basket',
          to: { name: 'services' },
        },
          {
          title: 'About',
          icon: 'help',
          to: { name: 'about' },
        },
        {
          title: 'Contact',
          icon: 'phone',
          to: { name: 'contact' },
        },
      ],
    }
  },
}
</script>
<style>

.fade-enter-active{
transition:all 3s ease,


}
.fade-leave-active{

transition:all 2s ease,

}








/* cards */
.card:hover{
transition:all 2s;
transform: scale(120%);
}
.links:hover{
transition:all 2s;
transform: scale(120%);
}


.footer{
bottom: 0;
min-width:100vw;
position:fixed;
}
</style>