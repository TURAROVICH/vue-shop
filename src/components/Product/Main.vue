<template>
<div>
    <div class="main">
        <div class="nav">
       <div class="title">
           Зимняя распродажа
       </div>

       <div class="discount">
           СКИДКИ ДО 90%
       </div>

       <button @click="show = !show">
           купить
       </button>
        </div>

        <div class="boots">
                <img id="product-photo" src="@/assets/boots.png" alt="">
        </div>

        <div class="price">
           <div class="old-price">9900руб.</div>
           <div class="discount-with">1900руб.</div>
        </div>
    </div>

<div class="fixed-modal" v-if="show">
         <Modal @close="show=false"/>
</div>

</div>
</template>

<script>
import Modal from './Modal'
export default {
    data:()=>({
         show:false
    }),
   components:{
       Modal
   },

}
</script>

<style scoped>
.fixed-modal{
    position: fixed;
    width: 100%;
    height: 100vh;
    top: 0;
    z-index:999;
}
button{
    transition: all .9s ease;
}
button:hover{
    background: rgb(207, 5, 5);
}
*{
    box-sizing: border-box;
    background-size: contain;
}
.old-price{
    
font-family: Montserrat;
font-style: normal;
font-weight: bold;
font-size: 24px;
line-height: 29px;
text-align: right;
letter-spacing: 0.05em;
text-decoration-line: line-through;
text-transform: uppercase;

color: #000000;
}
.discount-with{
    font-family: Montserrat;
font-style: normal;
font-weight: bold;
font-size: 42px;
line-height: 51px;
text-align: right;
letter-spacing: 0.02em;
text-transform: uppercase;

color: #D84033;
}
.nav div{
    margin:  20px 0;
}
.nav{
    display: flex;
    justify-content: left;
    align-items:flex-start;
    flex-direction: column;
    text-align: justify;
}
.title{
    
font-family: Montserrat;
font-style: normal;
font-weight: normal;
font-size: 30px;
line-height: 37px;
letter-spacing: 0.02em;

color: #000000;

}
.discount{
 white-space: nowrap;   
font-family: Montserrat;
font-style: normal;
font-weight: bold;
font-size: 55px;
line-height: 67px;
letter-spacing: 0.04em;

color: #000000;

}
.main{
    margin: 50px;
    display: flex;
}
button{
    width: 240px;
height: 55px;
background: #D7B399;
border-radius: 5px;
outline: none;
border:0;
cursor: pointer;
font-family: Montserrat;
font-style: normal;
font-weight: normal;
font-size: 16px;
line-height: 20px;
/* identical to box height */

letter-spacing: 0.03em;

color: #FFFFFF;
}

@media screen and (max-width:1150px){
    .discount{
        font-size: 45px;
    }
    #product-photo{
        width: 400px;
    }
}

@media screen and (max-width:1079px){
    .discount{
        font-size: 35px;
    }
    #product-photo{
        width: 350px;
    }
    .title{
        font-size: 25px;
    }
}



@media screen and (max-width:939px){
    .discount{
        font-size: 30px;
        letter-spacing: 0.01rem;
    }
    #product-photo{
        width: 300px;
    }
    .title{
        font-size: 20px;
        letter-spacing: 0.01rem;
    }
   
}



@media screen and (max-width:836px){
    .discount{
        font-size: 40px;
        letter-spacing: 0.01rem;
    }
    #product-photo{
        width: 500px;
    }
    .title{
        font-size: 30px;
        letter-spacing: 0.01rem;
    }
     .main{
        flex-direction: column-reverse;
        align-items: center;
        justify-content: center;
        text-align: center;
     
    }
    .old-price{
        font-size: 30px;
        margin-left: 30px;
    }
}

@media screen and (max-width:521px){
        #product-photo{
    width: 350px;
        }
}
</style>