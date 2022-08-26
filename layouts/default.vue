<template>
  <div class="layout">

  <h1 class="has-text-centered is-italic title is-4 has-text-warning has-text-weight-bold mt-3"> Hi!</h1>
      <h1
        class="has-text-centered is-italic title is-4 has-text-warning has-text-weight-bold mt-3"
      >
       "I Code and Design <span class="subtitle is-5 has-text-light is-italic is-underlined">beautiful and really simple things."</span>
      </h1>
    <section class="section " >
      <div class="columns is-multiline mx-auto">
        <aside class="column is-one-fifth">

          <ul class="menu-list is-flex-mobile mx-auto">
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

        <div class="column is-four-fifths">
          <transition name="fade">
          <Nuxt />
          </transition>
        </div>
      </div>
    </section>
    <footer class="main-footer mt-auto p-5">
      <div class="columns is-centered">
                 <div class="column mx-auto is-one-fifth" style="width:150px;">
         <b-image
       src="/logo.png"
       ratio="16by9"

       :responsive="responsive"
       is-rounded
       >

       </b-image>
      </div>



      </div>
         <div class="has-text-centered my-4">
        <p class="has-text-centered has-text-weight-semi-bold is-size-5"> Designed by <span class="has-text-warning is-italic is-bold"> Fidel C.</span>      <span>{{ new Date().getFullYear() }}</span>
      </p>
      </div>
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
background-image: linear-gradient(rgb(92, 11, 53),rgb(47, 3, 47));

}

body{
height:100%;
width: 100%;
background-image: linear-gradient(rgb(92, 11, 53),rgb(124, 8, 124));
display: flex;
flex-direction: column;
}

.layout{
  height:100%;
  width: 100%;
  background-image: linear-gradient(rgb(92, 11, 53),rgb(47, 3, 47));
  display: flex;
  flex-direction: column;


}
.main-footer{
  margin-top: auto;
  background-image: linear-gradient(rgb(47, 3, 47),black);
  min-width:100%;
  height:5%;
}

.container{
  padding: 2rem;
  display: flex;
  width: 100%;
  height: 100%;
  flex-direction: column;
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
