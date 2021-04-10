<template>
    <div class="products">
        <div class="container">
            <img src="@/assets/Tshirt.png" alt="">
            <div class="text">Lorem ipsum dolor sit amet...</div>
           <button><img src="@/assets/Arrow.svg" alt=""></button>
        </div>
    
     <div class="container">
            <img src="@/assets/Tshirt.png" alt="">
            <div class="text">Lorem ipsum dolor sit...</div>
           <button><img src="@/assets/Arrow.svg" alt=""></button>
        </div>

         <div class="container">
            <img src="@/assets/Tshirt.png" alt="">
            <div class="text">Lorem ipsum dolor sit amet ...</div>
           <button @click="$router.push({ name: 'Product', params: { id: '1' } })"><img id="arrow" src="@/assets/Arrow.svg" alt=""></button>
        </div>

    
    </div>
</template>

<style scoped>

button{
    transition: all .9s ease;
}
button:hover{
    background: rgb(207, 5, 5);
}
*{
    flex-wrap: wrap;
    box-sizing: border-box;
}
.products{
    text-align: center;
    margin: 10px 200px;
    display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 10px;
  grid-auto-rows: minmax(100px, auto);
}
.container{
background: #F4F4F4;
}
button{
    outline: none;
    border-radius: 2px;
    background: #D7B399;
    width: 100%;
    height: 30px;
    border: 0;
    cursor: pointer;
}
#arrow{
   transition: all 2s ease;
}
.text{
       
font-family: Montserrat;
font-style: normal;
font-weight: bold;
}
@media screen and (max-width:1100px){
    .products{
          margin: 10px 50px;
    }
}

@media screen and (max-width:910px){
    .products{
          margin: 10px 50px;
          display: flex;
          flex-direction: column;

    }
}

@media screen and (max-width:576px){
    .products{
          margin: 10px 15px;
          display: flex;
          flex-direction: column;

    }
}
</style>