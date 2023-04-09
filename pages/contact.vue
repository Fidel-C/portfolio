<template>
  <div  class="page">
    <div class="columns is-centered is-multiline is-mobile p-2" style="border-radius:30%;" >
      <div class="column">
        <div style="width: 100px;">
          <a href="mailto:fidelchukwunyere@gmail.com"  target="_blank" class="has-text-light"
            ><b-image src="/email.png" class="socials"> </b-image>
          </a>
        </div>
      </div>

      <div class="column ">
        <div style="width:100px;" >
          <a href="https://wa.me/+2347064620806" target="_blank" class="has-text-light "
            ><b-image src="/whatsapp.png" class="socials"> </b-image>
          </a>
        </div>
      </div>

      <div class="column ">
        <div style="width: 100px;">
          <a href="https://m.me/febuka1" target="_blank"  class="has-text-light"
            ><b-image src="/messenger.png" class="socials"> </b-image>
          </a>
        </div>
      </div>
      <div class="column ">
        <div style="width: 100px;">
          <a href="https://t.me/@Sponkyy" target="_blank"  class="has-text-light"
            ><b-image src="/telegram.png" class="socials"> </b-image>
          </a>
        </div>
      </div>
    </div>
 
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: `PrettyQode | ${this.$route.name}`
    }
  },
}
</script>
<style>
.socials:hover{
  transition:all 1s;
transform:scale(120%);
}
</style>
