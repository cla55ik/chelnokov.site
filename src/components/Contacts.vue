<template>
    <div class="contacts">
        <div v-for="(contact, index) in contacts" v-bind:key="index">
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

    .contacts{
        padding: 25px;
        border: 2px solid #1A1D23;
        border-radius: 25px;
    }

</style>