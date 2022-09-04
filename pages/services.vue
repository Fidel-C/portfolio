<template>
  <section class="container">

    <div class="columns mb-4 is-centered is-multiline is-mobile mx-auto">
      <div class="column  is-one-quarter-desktop is-half-tablet" v-for="service in services" :key="service.slug">
        <Card :title="service.title"  :src="service.imgurl"  :ratio="'16by9'" style="height:230px;">

          <template #footer>

                 <b-button
              @click="getService(service)" class="is-dark is-small has-text-centered">Read more...</b-button>

          </template>

        </Card>
      </div>
    </div>


    <!-- child view -->

<b-modal v-model="showchild" class="p-2" animation="fade">
    <section class="active is-justify-content-center has-text-light">
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
      title: `PrettyQode | ${this.$route.name}`,
    }
  },

  data() {
    return {
        service:null,
        showchild:false,
      services: [
        {
          title: 'Backend',
          slug: 'backend-end-services',
          imgurl: '/backend.jpg',
          details:"Backend development is about the ‘behind-the-scene’ functionality of web or mobile applications. It is the code that runs in the server, it powers and connects the app to a database. Backend development works hand-in-hand with the frontend to deliver the final product to the end user."
        },
        {
          title: 'Frontend',
          slug: 'front-end-services',
          imgurl: '/frontend.jpg',
          details:'While backend development is focused on the server, database and the internal functionality of a web or mobile app, frontend development builds and structures the interface,which determines how the web/mobile app looks to the end users.'
        },
        {
          title: 'Logo Design',
          slug: 'logo-design',
          imgurl: '/logoDesign.jpg',
          details:'A logo gives your brand a distinctive pictorial identity. You should consider getting one for your brand.'
        },
        { title: "Projects Showcase",
         slug: 'my-projects', imgurl: '/logo.png' ,
         details:'Links to some of my projects',
         projects:[
          {url:'https://mobiledata.com.ng',desc:'VTU website built with Django'},
          {url:'https://onqode-store.netlify.app',desc:'E-commerce webapp built with Django Rest Framework and VueJS'}
         ]
         },
         { title: "More To Come",
         slug: 'more-services', imgurl: '/logo.png' ,
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

