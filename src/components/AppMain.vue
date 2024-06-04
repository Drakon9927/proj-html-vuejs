<template>
    <main>
      <div class="container-fluid full-width-container mt-5">
        <div class="col-12">
          <p class="text-center fs-6 text-danger ">CHOOSE YOUR FLAVOR</p>
          <h2 class="text-center">THE BEST PIZZA MENU IN TOWN</h2>
          <p class="text-center">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus fuga soluta itaque quisquam libero nisi explicabo, adipisci nostrum omnis! Soluta nihil ab voluptate incidunt laboriosam debitis? Vel suscipit quaerat amet.
          </p>
        </div>
        <div class="row text-left g-0">
          <div class="col-2 mb-4" v-for="(pizza, index) in pizzas" :key="index">
            <div class="card no-border">
              <img :src="pizza.imageUrl" class="card-img-top" alt="Image of pizza">
              <div class="card-body">
                <h5 class="card-title">{{ pizza.name }}</h5>
                <p class="card-text" v-html="formatPrice(pizza.price)"></p>
              </div>
            </div>
          </div>
        </div>
      </div>

     <!-- Container 2  -->
      <div class="container-fluid full-width-container my-3 mystarbg">
        <div class="row g-0">
            <div class="col-6 bigpadding ">
                <p class="fs-6 text-danger ">MADE WITH LOVE</p>
                <h2 class="text-white mb-3">DELISH PIZZA DEALS</h2>

                 <div class="row g-0 fs-4">
                            <div class="div text-white w-auto ">
                                <span class="text-danger">02</span><br>
                                <span>NOV</span>
                            </div>

                            <div class="div text-white w-auto ms-4">
                        <span>TRADITIONAL NEAPOLITAN PIES IN</span> <br>
                        <span>KYOTO PIZZA MERCATO</span> <br>
                        <span class="text-danger fs-6">204 E. Pizzetta Tommaso</span>

                           </div>
                </div>

                <hr class="dotted-hr w-75">

                <div class="row g-0 fs-4">
                            <div class="div text-white w-auto ">
                                <span class="text-danger">03</span><br>
                                <span>NOV</span>
                            </div>

                            <div class="div text-white w-auto ms-4">
                        <span>TERAZZA PATIO DINING SPACE</span> <br>
                        <span>OPENING THIS WEEKEND</span> <br>
                        <span class="text-danger fs-6">204 E. Pizzetta Tommaso</span>
                                
                           </div>
                </div>

                <hr class="dotted-hr w-75">

                <div class="row g-0 fs-4">
                            <div class="div text-white w-auto ">
                                <span class="text-danger">05</span><br>
                                <span>NOV</span>
                            </div>

                            <div class="div text-white w-auto ms-4">
                        <span>SIENNA PRIVATE DINING ROOM WITH</span> <br>
                        <span>STEPHANE BRUNN</span> <br>
                        <span class="text-danger fs-6">204 E. Pizzetta Tommaso</span>
                                
                           </div>
                </div>
          
            </div>

            <div class="col-6 myimgbg">
                
            </div>
        </div>

      </div>
    </main>
  </template>
  
  <script>
  export default {
    data() {
      return {
        pizzas: [
          { name: 'Fiori di zucca', price: '$7.00 - $50.00', imageUrl: '/public/img/h3-product-img-2a-150x150.png' },
          { name: 'Valdostana', price: '$55.00', imageUrl: '/public/img/h3-product-img-6a-100x100.png' },
          { name: 'Pizza Tartufata', price: '$45.00', imageUrl: '/public/img/h3-product-img-4a-150x150.png' },
          { name: 'Francescana', price: '$25.00', imageUrl: '/public/img/h3-product-img-5a-150x150.png' },
          { name: 'Campagnola', price: '$50.00 - $95.00', imageUrl: '/public/img/h3-product-img-3a-150x150.png' },
          { name: 'Bismark', price: '<del>$35.00</del> $30.00', imageUrl: '/public/img/h3-product-img-1a-100x100.png' }
        ]
      };
    },
    methods: {
      formatPrice(price) {
        return price;
      }
    }
  }
  </script>
  
  <style>
.full-width-container {
  width: 100% !important;
  padding-left: 0 !important;
  padding-right: 0 !important;
}
  
  .no-border {
    border: none;
  }
  
  .card-img-top{
    height: 200px;
    width: 200px;
    
  }

  .mystarbg{
    background-image: url(/public/img/cielostellato.PNG);
  }

  .bigpadding{
    padding: 100px;
  }

  .dotted-hr {
  border: 0;
  border-top: 3px dotted yellow; 
  margin: 2rem 0; 
}

.myimgbg{
    background-image: url(/public/img/h3-img-5a.jpg);
    background-size: cover;
}
  </style>