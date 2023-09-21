<template>
  <div class="container mt-5 pt-5 pb-4">
    <p class="text-center pb-1 RalewayFont main_title" >{{ Frase_Principal.titulo }}</p>
    <p class="text-center fs-2 SatisfyFont pb-5 " style="color: #8c8989;">Ingredientes Locales, Recetas Mundiales</p>
    <div class="row">
      <div class="col-12 col-lg-6 d-flex justify-content-center align-items-center">
        <p class="multiline-content text-center RalewayFont lh-lg mt-1 main_description">{{ Frase_Principal.descripcion }}</p>
      </div>
      <div class="col-12 col-lg-6 d-flex justify-content-center align-items-center">
        <img class="img-fluid" src="../assets/logo/Plato_La_Madre.png" alt="None">
      </div>
    </div>
    
    <div class="my-5 container-fluid d-flex align-items-center justify-content-center">
      <img class="img-fluid main_logo" src="../assets/logo/Logo_La_Madre.webp" alt="None">
      <img src="../assets/logo/La_Madre_Del_Pollo.png" width="125" class="img-fluid ms-lg-5 img-responsive img-fluid-sm img-fluid-lg main_logo" alt="...">
    </div>
  </div>
</template>

<script>
import { inject } from 'vue';
export default {
  setup() {
    const data = inject('$data');
    const Frase_Principal = data.Frase_Principal[0];
    
    return {
      Frase_Principal,

    };
  }
};
</script>

<style>
@media (max-width: 580px) {
    .main_title{
    font-size: 43px;

    }
    .main_description{
      font-size: 15px;
      margin-top: 30px;
    }
    .main_logo{
      width: 115px;
    }
}

@media (min-width: 581px) and (max-width: 992px){
    .main_title{
    font-size: 57px;
    margin-top: 30px;
    }
    .main_description{
      font-size: 19px;
      margin-top: 30px;
    }
    .main_logo{
      width: 120px;
      margin-top: 20px;
      margin-bottom: 50px;
    }
}
@media(min-width: 993px){
    .main_title{
    font-size: 85px;

    }
    .main_description{
      font-size: 18px;
      margin-top: 30px;
      margin-bottom: 10px;
    }
    .main_logo{
      width: 130px;
      margin-top: 20px;
      margin-bottom: 80px;
    }
}

</style>