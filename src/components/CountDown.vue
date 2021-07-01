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
            <div class="title" >
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
            if (this.seconds < 10) {
                this.seconds = '0' + this.seconds;
                
            }

            if (this.minutes < 10) {
                this.minutes = '0' + this.minutes;
                
            }

            if (this.hours < 10) {
                this.minutes = '0' + this.hours;
            }

            if (this.days < 10) {
                this.minutes = '0' + this.days;
            }
           


        },
       
        
    },
}
</script>

<style scoped>

.item{
    text-align: center;
    

}


.wrapper{
    display: flex;
    justify-content: space-between;
    margin-top: 25px;
    margin-bottom: 30px;
}

.data{
    font-size: 36px;
    border-radius: 20px;
    background-color: #1A1D23;
    padding: 15px;
    color: white;
    margin-bottom: 10px;
}

.title {
    font-weight: 300;
    font-size: 18px;
}


@media screen and (min-width:1200px) {
    .wrapper{
       
        padding-right: 20%;
        padding-top: 20px;
    }


    .data{
        font-size: 56px;
        border-radius: 20px;
        
        padding: 15px;
        
        margin-bottom: 10px;
    }
    
}


</style>