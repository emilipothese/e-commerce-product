<template>
  <section>
    <div class="pictures">
      <img class="picture--big" src="../assets/image-product-1.jpg" alt="">
    </div>
    <div class="text">
      <small>Sneaker Compagny</small>
      <h1>Fall limited edition sneakers</h1>
      <p class="description">These low-profile sneakers are your perfect casual wear
  companion. Featuring a durable rubber outer sole, they'll
  withstand everything the weather can offer.</p>
      <p class="description__price">$125.00 <span class="description__pourcentage">50%</span></p>
      <p class="description__price--sold">$250</p>
      <div class="cart">
        <button class="cart__btn"><img src="../assets/icon-cart.svg" alt=""> Add to cart</button>
      </div>
    </div>
  </section>
</template>


<style scoped>
  section {
    display: flex;
    margin: 50px 20px;
  }

  .pictures {
    width: 50%;
  }

  .text {
    width: 50%;
    text-align: left;
    margin-left: 20px;
  }

  .picture--big {
    width: 100%;
    border-radius: 10px;
  }

  h1 {
    text-transform: capitalize;
    font-weight: 900;
    font-size: 2.5rem;
    line-height: 2.8rem;
    margin: 10px 0;
  }

  small {
    color: hsl(26, 100%, 55%);
    text-transform: uppercase;
    font-weight: 700;
  }

  .description {
    color: hsl(219, 9%, 45%);
  }

  .description__price {
    font-weight: 900;
    font-size: 1.8rem;
    color: #2c3e50;
    display: flex;
    align-items: center;
    margin: 10px 0 0 0;
  }

  .description__pourcentage {
    color: hsl(26, 100%, 55%);
    font-size: 1rem;
    background-color: hsl(25, 100%, 94%);
    padding: 2px 5px;
    border-radius: 3px;
    margin-left: 10px;
  }

  .description__price--sold {
    text-decoration: line-through;
    color: hsl(219, 9%, 45%);
    margin: 5px 0;
  }

  .cart__btn {
    background-color: hsl(26, 100%, 55%);
    border-radius: 7px;
    border: hsl(26, 100%, 55%);
    color: white;
  }
</style>
