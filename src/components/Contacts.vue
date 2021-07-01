<template>
    <div class="title">
      <h2>Связаться:</h2>
    </div>
    <div class="contact">
        <div class="item" v-for="(contact, index) in contacts" v-bind:key="index">
            
            <a :href="contact.link">{{ contact.name }}</a>
        </div>
    </div>
    <div class="soсial">
      <a href=""><img src="~@/assets/img/telegram1.svg" alt=""></a>
      <a href=""><img src="~@/assets/img/whatsapp.svg" alt=""></a>
      <a href=""><img src="~@/assets/img/ya_uslugi_.svg" alt=""></a>
    </div>
</template>

<script>
export default {

    data(){
    return{
      contacts:[
        {name:'+79102814760', link:'tel:+79102814760'},
       
        {name:'ivan5420@yandex.ru', link:'mailto:ivan5420@yandex.ru'},
      ]
    }
  },
    
}
</script>

<style scoped>



  a{
    color: #1A1D23;
    text-decoration: none;
    
  }

  .title{
    margin-bottom: 40px;
  }

  .item{
    margin: 10px 0px;
  }

  .soсial{
    margin-top: 40px;
    display: flex;
    justify-content: space-around;
  }

  .soсial img{
    width: 30px;
    height: auto;
    object-fit: contain;
    margin-right: 20px;
    
  }

  h2{
    font-size: 24px;
  }

  @media screen and (min-width:1200px) {
    h2{
      font-size: 24px;
    }

    .social{
      justify-content: flex-start;
    }
  }

</style>