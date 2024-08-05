<template>
    <!-- alt-bilesen adında bir bileşeni kullanıyor -->
    <alt-bilesen>
      
      <!-- form-header slot'u için içerik tanımlanıyor -->
      <template #form-header>
        <h2>Giriş Formu 2</h2>
        <p>Giriş yapabilmek için lütfen formu doldurun</p>
      </template>
  
      <!-- form-elements slot'u için içerik tanımlanıyor -->
      <template #form-elements>
        <label for="email">E-Posta</label>
        <input type="email" name="email" placeholder="E-posta adresinizi giriniz">
  
        <label for="password">Şifre</label>
        <input type="password" name="password" placeholder="Şifrenizi giriniz">
      </template>
  
      <!-- form-controls slot'u için içerik tanımlanıyor -->
      <template #form-controls>
        <button>Giriş Yap</button>
      </template>
  
      <!-- Varsayılan slot (isim verilmemiş slot) için içerik tanımlanıyor -->
      <template>
        <p>Tüm Hakları Saklıdır</p>
      </template>
  
    </alt-bilesen>
</template>

<script>
// altBilesen bileşenini import ediyor
import altBilesen from './alt-bilesen.vue'

export default {
  // altBilesen bileşenini kaydediyor
  components: {
    "alt-bilesen": altBilesen
  },
  data() {
    return {
      // Burada veri tanımları yapılabilir
    }
  }
}
</script>
