  <template>

<div class="layout">

      <div class="columns is-multiline mx-auto">

        <aside class="column is-one-fifth nx-auto">

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
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;

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


.layout,body,html{

background-image: radial-gradient(orange 10%,black 90%);
color: wheat;
height:100dvh;
width: 100dvw;
margin:0 0;

}


.page{
  padding: 10px 20px;
}

.main-footer {
  bottom: 0;
  justify-self: end;
  left:20px;
  right: 20px;
  background-image:radial-gradient(orange 10%,black 90%);
  color: wheat;
  padding:0 10px;
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
