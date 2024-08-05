<template>
    <form action="#">
      <!-- Ana konteyner -->
      <div class="container">
          <!-- İç konteyner -->
          <div class="container-inner">
  
              <!-- Form başlık kısmı -->
              <div class="form-header">
                  <slot name="form-header"></slot>
              </div>
  
              <!-- Form elemanları -->
              <div class="form-elements">
                  <div class="form-elements-inner">
                      <slot name="form-elements"></slot>
                  </div>
              </div>
  
              <!-- Form kontrolleri (butonlar vs.) -->
              <div class="form-controls">
                  <div class="form-controls-inner">
                      <slot name="form-controls"></slot>
                  </div>
              </div>
  
              <!-- Faydalı linkler -->
              <div class="useful-links">
                  <ul>
                      <li><a href="#">Link 1</a></li>
                      <li><a href="#">Link 2</a></li>
                      <li><a href="#">Link 3</a></li>
                      <li><a href="#">Link 4</a></li>
                  </ul>
              </div>
  
          </div>
      </div>
    </form>
  </template>
  
  <style scoped>
  /* Ana konteynerin genişliği ve ortalanması */
  .container {
      widows: 100%; 
      margin: 0 auto;
  }
  
  /* İç konteynerin genişliği, ortalanması, kenarlığı ve iç boşluğu */
  .container-inner {
      width: 50%; 
      margin: 0px auto; 
      border: 1px solid #e2e2e2; 
      padding: 15px;
  }
  
  /* Form başlığının stil ayarları */
  .form-header {
      text-align: center; 
      border-bottom: 1px solid #e2e2e2; 
      margin-top: 35px;
  }
  
  /* Form elemanlarının yerleşimi ve üst boşluğu */
  .form-elements {
      display: flex; 
      justify-content: center; 
      margin-top: 35px;
  }
  
  /* Form elemanlarının iç konteyner genişliği */
  .form-elements-inner {
      width: 50%;
  }
  
  /* Slot içindeki input elemanlarının genişliği, kenarlığı, yüksekliği, köşe yuvarlaması, üst ve alt boşlukları ve iç boşluğu */
  :slotted(input) {
      width: 100%; 
      border: 1px solid #e2e2e2; 
      height: 35px; 
      border-radius: 5px; 
      margin: 5px 0 15px 0; 
      padding-left: 15px;
  }
  
  /* Form kontrollerinin (butonlar vs.) yerleşimi, hizalanması ve boşlukları */
  .form-controls {
      display: flex; 
      justify-content: center; 
      text-align: right; 
      margin: 15px;
  }
  
  /* Form kontrollerinin iç konteyner genişliği */
  .form-controls-inner {
      width: 50%;
  }
  
  /* Slot içindeki butonların yüksekliği, kenarlığı ve iç boşluğu */
  :slotted(button) {
      height: 35px; 
      border: 1px solid #e2e2e2; 
      padding: 0px 15px;
  }
  
  /* Faydalı linklerin yerleşimi ve üst kenarlığı */
  .useful-links {
      display: flex; 
      justify-content: center; 
      border-top: 1px solid #e2e2e2;
  }
  
  /* Liste stil ayarları ve üst boşluğu */
  ul {
      list-style-type: none; 
      margin: 15px 0 0 0;
  }
  
  /* Liste elemanlarının yerleşimi ve sağ boşluğu */
  ul li {
      float: left; 
      margin-right: 5px;
  }
  
  /* Linklerin stil ayarları ve üzerine gelindiğinde renk değişimi */
  ul li a {
      text-decoration: none; 
      color: #666;
  }
  ul li a:hover {
      color: #000;
  }
  </style>
  