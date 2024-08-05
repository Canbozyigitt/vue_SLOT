<template>
  <!-- Bileşenler arasında geçiş yapmayı sağlar, geçiş yapan bileşenleri bellekte tutar -->
  <keep-alive>
    <!-- Dinamik bileşen, "component" değişkenine bağlı olarak form-one veya form-two'yu render eder
    keep-alive= Bileşenler arasında geçiş yaparken, geçiş yapılan bileşenlerin bellekte saklanmasını sağlar. Bu, bileşenlerin durumunu korumaya yardımcı olur ve performansı artırabilir.-->
    <component v-bind:is="component"></component>
  </keep-alive>

  <!-- Form 1'i göstermek için bir düğme -->
  <button v-on:click="component='form-one'">Form 1'i Göster</button>
  
  <!-- Form 2'yi göstermek için bir düğme -->
  <button v-on:click="component='form-two'">Form 2'yi Göster</button>
</template>

<script>
// İki form bileşenini import eder
import formOne from './components/form-one.vue'
import formTwo from './components/form-two.vue'

export default {
  components: {
    // Bileşenleri tanımlar
    "form-one": formOne,
    "form-two": formTwo
  },
  data() {
    return {
      // Varsayılan olarak gösterilen bileşeni ayarlar
      component: 'form-two'
    }
  }
}
</script>

<style scoped>
/* Stil tanımlamaları buraya eklenebilir */
</style>
