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
                       <CountDown/>
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
import CountDown from '@/components/CountDown.vue'

export default {
    props:['contacts'],
    components:{
        Contacts, CountDown
    }
    
}

</script>

<style scoped>
    

    .header{
        display: block;
        align-items: center;
        padding: 50px 0px;
        text-align: center;
    }

    .ivan{
        margin-left: 20px;
        font-weight: normal;
        font-size: 24px;
        line-height: 28px;
    }

    h1{
        
        font-weight: normal;
        font-size: 32px;
        line-height: 48px;
        margin:0;
        text-align: center;
    }

    p{
        font-style: normal;
        font-weight: 300;
        font-size: 20px;
        line-height: 23px;
        margin-bottom: 20px;
    }

    .main p{
        display: none;
    }


    .content{
        display: block;
    }

  

    .main{
        width: 100%;
    }

    .contacts{
        text-align: center;
        width: auto;
        margin-left: 0%;

        padding: 35px;
        border: 2px solid #1A1D23;
        border-radius: 25px;
    }

    .timer .title{
        text-align: center;
        margin-top: 15px;
    }

    @media screen and (min-width:1200px) {

         .header{
            display: flex;
            align-items: center;
            padding: 50px 0px;
            
        }


        h1{
            
            font-size: 68px;
            line-height: 84px;
            text-align: left;
        }

        p{
            font-size: 20px;
            line-height: 23px;
        }

          .main p{
            display: block;
        }

        .ivan{
            margin-left: 25px;
            
            font-size: 24px;
            line-height: 28px;
        }

        .timer .title{
            margin-top: 70px;
            text-align: left;
            
        }

        .main{
            width: 70%;
        }

        .contacts{
            text-align: left;
            width: 25%;
            margin-left: 5%;

            padding: 35px;
            border: 2px solid #1A1D23;
            border-radius: 25px;
        }

        .content{
            display: flex;
        }

          
    }

    

</style>