<template>
    <div class="wrapper">
        <div class="item">
            <div class="data">
                {{ days }}
            </div>
            <div class="title">
                дней
            </div>
        </div>
        <div class="item">
            <div class="data">
                {{ hours }}
            </div>
            <div class="title">
                часов
            </div>
        </div>
        <div class="item">
            <div class="data">
                {{ minutes }}
            </div>
            <div class="title">
                минут
            </div>
        </div>
        <div class="item">
            <div class="data">
                {{ seconds }}
            </div>
            <div class="title">
                секунд
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data: function(){
        return{
            dateEnd: new Date(2021,6,16),
            dateNow: null,
            timeToLeft: null,
            days:null,
            hours:null,
            minutes:null,
            seconds:null
        }
    },
    mounted:function(){
        //this.getTimeToLeft();
        setInterval(() => {
            this.getTimeToLeft();
            this.parseTimeToLeft(this.timeToLeft);
            
        }, 1000); 
        
        //this.getHours(this.timeToLeft);
    },
    methods:{
        getTimeToLeft: function(){
            this.dateNow = new Date();
            this.timeToLeft = this.dateEnd - this.dateNow;
           
        },
        parseTimeToLeft: function(ttl){
            let date = new Date();
            
            date.setTime(ttl);
            this.days = date.getDate();
            this.hours = date.getHours();
            this.minutes = date.getMinutes();
            this.seconds = date.getSeconds();
           


        },
       
        
    },
}
</script>

<style scoped>

.wrapper{
    display: flex;
}

</style>