<template>
  <div class="layout">

    <section class="container">
      <div class="columns is-multiline mx-auto">

        <aside class="column is-one-fifth">

          <ul class="menu-list is-flex-mobile mx-auto">
            <li v-for="(item, key) of items" :key="key" class="has-text-weight-bold links">
              <NuxtLink :to="item.to" exact-active-class="is-active">
                <b-icon :icon="item.icon" class="has-text-warning" />
                {{ item.title }}
              </NuxtLink>
            </li>
          </ul>
        </aside>

        <div class="column is-four-fifths">
          <h1 class="has-text-centered is-italic title is-4 has-text-warning has-text-weight-bold mt-3"> Hi!</h1>
          <h1 class=" has-text-centered is-italic title is-4 has-text-warning has-text-weight-bold mt-3">
            "I Code and Design <span class="subtitle is-5 has-text-light is-italic is-underlined typing">beautiful and
              really simple things."</span>
          </h1>
          <transition name="fade">
            <Nuxt />
          </transition>
        </div>
      </div>
    </section>
    <footer class="main-footer">
      <div class="columns is-centered is-align-items-center">
        <div class="column">
          <div class="mx-auto" style="width:152px;">
            <b-image src="/logo.png" ratio="16by9" :responsive="responsive" is-rounded>

            </b-image>
          </div>
        </div>


        <div class="column">
          <div class="has-text-centered">&copy; 2020 - {{ new Date().getFullYear() }}</div>
        </div>
      </div>

    </footer>
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



body {
   background-image: radial-gradient(black,orange);
  color: wheat;
  overflow:hidden;

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

.layout {
  height: 100dvh;
  width: 100vw;
  display: flex;
  flex-direction:column;
}

.container {
  width: 100vw;
  height: 100dvh;
  flex-grow: 1;
  padding:1rem;

}

.main-footer {
  width: 100vw;
  background-image: radial-gradient(orange,black);
  color: wheat
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
