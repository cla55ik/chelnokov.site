<template>
    <div class="title">
      <h2>Связаться:</h2>
    </div>
    <div class="contact">
        <div class="item" v-for="(contact, index) in contacts" v-bind:key="index">
            <a :href="contact.link">{{ contact.name }}</a>
        </div>
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

  .item{
    margin: 10px 0px;
  }

  @media screen and (min-width:1200px) {
    h2{
      font-size: 24px;
    }
  }

</style>