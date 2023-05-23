  <template>

<div class="layout">

      <div class=" columns  mb-5 is-multiline mx-auto">

        <aside class="column is-one-fifth mx-auto">

          <div class="menu-list is-flex-mobile mx-auto"  >
            <ul v-for="(item, key) of items" :key="key" class="has-text-weight-bold links mx-auto">
              <NuxtLink :to="item.to" exact-active-class="is-active">
                <b-icon :icon="item.icon" class="has-text-warning" />
                {{ item.title }}
              </NuxtLink>
            </ul>
          </div>
        </aside>

        <div class="column is-four-fifths">
          <h2 class="has-text-centered is-italic title is-4 has-text-warning has-text-weight-bold mt-3"> Hi!</h2>
          <h3 class=" has-text-centered is-italic title is-4 has-text-warning has-text-weight-bold mt-3">
            "I Code and Design <span class="subtitle is-5 has-text-light is-italic is-underlined typing">beautiful and
              really simple things."</span>
          </h3>
          <transition name="fade">
            <Nuxt />

          </transition>

        </div>
      </div>


     <div class="main-footer" >
            <div  style="width:70px;height:40px;">
              <b-image src="/logo.png" ratio="16by9" :responsive="responsive" is-rounded> </b-image>
            </div>


            <div> &copy; 2020 - {{ new Date().getFullYear() }} </div>

          </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      responsive: true,
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
html{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  height:100%;
  position:relative;
}

body{
min-height: 100%;
box-sizing: border-box;
padding:0;
margin:0;
background-image:radial-gradient(orange 10%,black 90%);

}
.layout{
min-height: 100%;
box-sizing:border-box;
margin:0;
padding:0;

}
.is-active {
  color: purple;
}

.fade-enter-active {
  transition: all 1s ease-in,
}

.fade-leave-active {
  transition: all 1s ease-in-out,
}






.main-footer {
  position:absolute;
  top:auto;
  bottom: 0;
  left:0;
  right:0;
  background-image:radial-gradient(orange 10%,black 90%);
  color: wheat;
  display:flex;
  justify-content: center;
  align-items: center;
}



/* cards */
.card:hover {
  transition: all 1s;
  transform: scale(120%);
}


.links:hover {
  transition: all 1s;
  transform: scale(120%);
}


.typing {
  animation: typing 3s linear 2;
}


@keyframes typing {
  from {
    width: 0;
  }

  to {
    width: 100%;
  }
}
</style>
