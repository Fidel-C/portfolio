<template>
  <section class="container" >

  <div class="columns is-centered mx-auto" style="border-radius:30%;">
<div class="column">
  <h1 class="title is-2 has-text-warning has-text-centered is-italic">All<span class="has-text-light is-underlined">things beautiful</span> </h1>
       <b-icon icon="handshake" class="has-text-warning has-text-centered" size="is-large"></b-icon>
</div>

<div class="column">

        <b-carousel :arrow="arrow">
          <b-carousel-item  v-for="(item, i) in items" :key="i">
            <section :class="`hero is-${item}`">

           <div class="flex is-justify-content-center has-text-centered" style="max-height:200px;max-width:300px;">
             <div class="has-text-centered mx-auto">
                   <b-image
               :src="item.imgurl"
               :responsive="responsive"
               ratio="16by9" >

               </b-image>
             </div>
           </div>
            </section>

          </b-carousel-item>



        </b-carousel>

     </div>

  </div>




  </section>
</template>

<script>
export default {

  head(){
return{
  title:`Onqode | Home`
}
  },


data(){

  return{
   items: [
  {imgurl:'/logo.png',},
  {imgurl:'/email.png',},
  {imgurl:'/frontend.jpg',},
  {imgurl:'/backend.jpg',},
  {imgurl:'/messenger.png',},
  {imgurl:'/telegram.png',},
  {imgurl:'/whatsapp.png',},

],
arrow:true,
responsive:true
  }
},




}
</script>


