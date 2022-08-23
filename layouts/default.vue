<template>
  <div class="layout">
    <section class="section is-justify-content-center is-align-items-center">
                      <h1 class="has-text-centered is-italic title is-4 has-text-warning has-text-weight-bold mt-3"> Hi!</h1>
      <h1
        class="has-text-centered is-italic title is-4 has-text-warning has-text-weight-bold mt-3"
      >
       "I Code and Design <span class="subtitle is-5 has-text-light is-italic is-underlined">beautiful and really simple things."</span>
      </h1>
    </section>
    <section class="section " >
      <div class="columns">
        <aside class="column is-2 section m-5 p-2 is-flex is-align-items-center is-justify-content-between">

          <ul class="menu-list is-flex-mobile">
            <li
              v-for="(item, key) of items"
              :key="key"
              class="has-text-weight-bold links"
            >
              <NuxtLink :to="item.to" exact-active-class="is-active has-background-dark" style="background-image: linear-gradient(rgb(47, 3, 47),black);">
                <b-icon :icon="item.icon" class="has-text-warning" />
                {{ item.title }}
              </NuxtLink>
            </li>
          </ul>
        </aside>

        <div class="column is-10 p-2 mb-4">
          <transition name="fade">
          <Nuxt />
          </transition>
        </div>
      </div>
    </section>
    <footer class="is-flex is-flex-direction-column main-footer has-background-black has-text-light is-italic is-justify-content-center is-align-items-center">
            <div class="is-justify-content-center mb-5"  style="width:100px">
         <b-image
       src="/logoDark.png"
       ratio="16by9"
       :responsive="responsive"
       is-rounded
       >

       </b-image>
      </div>

      <p class="has-text-centered has-text-weight-semi-bold is-size-5"> Designed by
        <span class="has-text-warning has-text-weight-bold">Fidel C. </span> &copy <p class="has-text-warning has-text-weight-bold">{{ new Date().getFullYear() }}
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

*{
  margin:0;
  padding:0;
  box-sizing:border-box;
}

.fade-enter-active{
transition:all 2s ease-in,


}
.fade-leave-active{

transition:all 2s ease-in-out,

}

html{
  height:100%;
  width:100%;
  background-image: linear-gradient(rgb(240, 230, 230),rgb(47, 3, 47));

}

body{
height:100%;
width: 100%;

}

.layout{
  height:100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  background-image: linear-gradient(rgb(92, 11, 53),rgb(47, 3, 47));


}
.main-footer{
  margin-top: auto;
  background-image: linear-gradient(rgb(47, 3, 47),black);
}








/* cards */
.card:hover{
transition:all 1s;
transform: scale(120%);
}
.links:hover{
transition:all 1s;
transform: scale(120%);
}



</style>
