<template>
  <section class="section has-background-black" style="border-radius:30%;">
   <div class="level is-align-items-center is-justify-content-space-around">
                          
     <div class="container is-flex is-justify-content-center">
 
       <h1 class="title is-2 has-text-warning has-text-centered-mobile is-italic">All<span class="has-text-light is-underlined">things beautiful</span> </h1>
       <b-icon icon="handshake" class="ml-3 has-text-warning" size="is-large"></b-icon>
   </div>

     <div class="container is-justify-content-center">
        <b-carousel :arrow="arrow">
          <b-carousel-item  v-for="(item, i) in items" :key="i">
            <section :class="`hero is-${item}`">

           <div class="hero-body">
             <div class="">
                   <b-image
               :src="item.imgurl"
               :responsive="responsive"
               ratio="16by9">

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
  {imgurl:'/logoDark.png',},

],
arrow:true,
responsive:true
  }
},
  



}
</script>
