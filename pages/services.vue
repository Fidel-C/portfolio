<template>
  <section class="container">

    <div class="columns is-centered is-multiline">
      <div class="column is-one-quarter-desktop is-full-mobile" v-for="service in services" :key="service.slug">
        <Card class="m-4 p-2 " :title="service.title" :src="service.imgurl" ratio="16by9" >
          <template #footer>
            <b-button
              @click="getService(service)">Read more...</b-button>
          </template>
        </Card>
      </div>
    </div>


    <!-- child view -->
   
<b-modal v-model="showchild" class="p-4" animation="fade">
    <section class="has-background-primary is-justify-content-center has-text-light">
  <NuxtChild :service="service" />
    </section> 
</b-modal>

  </section>
</template>
<script>
import Card from '~/components/Card.vue'
export default {
  components: { Card },
  head() {
    return {
      title: `Onqode | ${this.$route.name}`,
    }
  },

  data() {
    return {
        service:null,
        showchild:false,
      services: [
        {
          title: 'Backend Development',
          slug: 'backend-end-services',
          imgurl: '/backend.jpg',
          details:"Backend development is about the ‘behind-the-scenes’ functionality of web or mobile applications. It is the code that runs in the server, it powers and connects the app to a database. Backend development works hand-in-hand with the frontend to deliver the final product to the end user."
        },
        {
          title: 'Frontend Development',
          slug: 'front-end-services',
          imgurl: '/frontend.jpg',
          details:'While backend development builds the functionality of a web or mobile app, frontend development builds and structures the interface,which determines how the web/mobile app looks to the end users.'
        },
        {
          title: 'Logo Design',
          slug: 'logo-design',
          imgurl: '/logoDesign.jpg',
          details:'A logo gives your brand a distinctive pictorial identity. You should consider getting one for your brand.'
        },
        { title: "There's More",
         slug: 'more-services', imgurl: '/LogoDark.png' ,
         details:'It is a little beginning, but the idea is to add more quality content in the near-future, and God willing, we shall !!!'
         },
      ],

      arrow: true,
      responsive: true,
    }
  },
methods:{ 
    getService(obj){
    if(obj){
this.service=obj,
this.showchild=true
}

}
}

}
</script>

<style scoped>

</style>