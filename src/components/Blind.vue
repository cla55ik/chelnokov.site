<template>
    <div class="wrapper"> 
       <div class="header">
           <div>
               <img src="@/assets/img/logo-dark.svg" alt="">
           </div>
           <div class="ivan">
               Ivan Chelnokov
           </div>
       </div>
       <div class="content">
           <div class="main">
               <div>
                   <h1>Сайт на реконструкции</h1>
                   <p>Наш сайт находится на техническом обслуживании и скоро станет доступен</p>
               </div>
               <div class="timer">
                   <div class="title">
                       До старта осталось:
                   </div>
                   <div class="countdown">

                   </div>
               </div>
           </div>
           <div class="contacts" >

               <Contacts/>
              
           </div>
       </div>
    </div>
</template>

<script>

//import Contacts from './components/blind/Contacts.vue' 
import Contacts from '@/components/Contacts.vue'

export default {
    props:['contacts'],
    components:{
        Contacts
    }
    
}

</script>

<style scoped>
    

    .header{
        display: flex;
        align-items: center;
        padding: 50px 0px;
    }

    .ivan{
        margin-left: 20px;
        font-weight: normal;
        font-size: 24px;
        line-height: 28px;
    }

    h1{
        
        font-weight: normal;
        font-size: 24px;
        line-height: 28px;
        margin:0;
    }

    p{
        font-style: normal;
        font-weight: 300;
        font-size: 20px;
        line-height: 23px;
    }


    .content{
        display: flex;
    }

    @media screen and (min-width:1200px) {
        h1{
            
            font-size: 68px;
            line-height: 84px;
        }

        p{
            font-size: 20px;
            line-height: 23px;
        }

        .ivan{
            margin-left: 25px;
            
            font-size: 24px;
            line-height: 28px;
        }

        .timer .title{
            margin-top: 70px;
        }

        .main{
            width: 70%;
        }

        .contacts{
            width: 25%;
            margin-left: 5%;

            padding: 25px;
            border: 2px solid #1A1D23;
            border-radius: 25px;
        }

          
    }

    

</style>