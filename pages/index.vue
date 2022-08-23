<template>
  <section class="container" >
   <div class="p-4">

     <div class="p-2  is-justify-content-center" style="border-radius:30%;">


<div class="flex is-justify-content-between">
  <h1 class="title is-2 has-text-warning has-text-centered is-italic">All<span class="has-text-light is-underlined">things beautiful</span> </h1>
       <b-icon icon="handshake" class="has-text-warning has-text-centered" size="is-large"></b-icon>
</div>
<div class="section has-text-centered">
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
  {imgurl:'/logoDark.png',},

],
arrow:true,
responsive:true
  }
},




}
</script>
