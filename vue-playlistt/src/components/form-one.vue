<template>
    <!-- alt-bilesen adında bir bileşen kullanılıyor -->
    <alt-bilesen>
      
      <!-- form-header slot'u için içerik tanımlanıyor -->
      <template #form-header>
        <h2>Giriş Formu 1</h2>
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
  
      <!-- Varsayılan slot (herhangi bir isim belirtilmemiş slot) için içerik tanımlanıyor -->
      <template>
        <p>Tüm Hakları Saklıdır</p>
      </template>
  
    </alt-bilesen>
</template>

<script>
// altBilesen bileşeni import ediliyor
import altBilesen from './alt-bilesen.vue'

export default {
  // altBilesen bileşeni kaydediliyor
  components: {
    "alt-bilesen": altBilesen
  },
  data() {
    return {
      // Veri tanımları burada yapılabilir
    }
  }
}
</script>
