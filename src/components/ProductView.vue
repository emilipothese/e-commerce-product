<template>
  <section>
    <div class="pictures">
      <img class="picture--big" src="../assets/image-product-1.jpg" alt="">
      <div class="thumbnails">
        <img class="picture--small" src="../assets/image-product-1-thumbnail.jpg" alt="">
        <img class="picture--small" src="../assets/image-product-2-thumbnail.jpg" alt="">
        <img class="picture--small" src="../assets/image-product-3-thumbnail.jpg" alt="">
        <img class="picture--small" src="../assets/image-product-4-thumbnail.jpg" alt="">
      </div>
    </div>
    <div class="text">
      <small>Sneaker Compagny</small>
      <h1>Fall limited edition sneakers</h1>
      <p class="description">These low-profile sneakers are your perfect casual wear
  companion. Featuring a durable rubber outer sole, they'll
  withstand everything the weather can offer.</p>
      <p class="description__price">$125.00 <span class="description__pourcentage">50%</span></p>
      <p class="description__price--sold">$250.00</p>
      <div class="cart">
        <div class="num">
          <button @click="count--" class="cart__num">-</button>
          <p class="text__num">{{ count }}</p>
          <button @click="count++" class="cart__num">+</button>
        </div>
        <button class="cart__btn"><img src="../assets/icon-cart.svg" alt=""> Add to cart</button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      count : 0
    }
  },
}
</script>

<style scoped>
  section {
    display: flex;
    align-items: center;
    margin: 50px 20px;
  }

  .pictures {
    width: 50%;
  }

  .text {
    width: 50%;
    text-align: left;
    margin-left: 70px;
  }

  .picture--big {
    width: 100%;
    border-radius: 10px;
    margin-bottom: 20px;
  }

  .thumbnails {
    display: flex;
    justify-content: space-between;
  }

  .picture--small {
    width: 23%;
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
    margin: 5px 0 15px 0;
  }

  .cart {
    display: flex;
  }

  .cart__btn {
    background-color: hsl(26, 100%, 55%);
    border-radius: 7px;
    border: hsl(26, 100%, 55%);
    color: white;
    font-weight: 700;
    font-size: 1rem;
    padding: 15px 0;
    width:60%;
  }

  .cart__btn:hover {
    background-color: hsl(220, 13%, 13%);
    cursor: pointer;
    transition: all .3s ease-out;
  }

  .cart__btn img {
    width: 7%;
  }

  .num {
    display: flex;
    width:40%;
    margin-right: 10px;
  }

  .cart__num {
    background-color: hsl(230, 5%, 95%);
    border: none;
    width:30%;
    font-weight: 700;
    color: hsl(26, 100%, 55%);
    font-size: 1.5rem;
    transition: all .3s ease-out;
  }

  .cart__num:hover {
    background-color: hsl(220, 14%, 75%);
    cursor: pointer;
  }

  .text__num {
    background-color: hsl(230, 5%, 95%);
    width:40%;
    padding: 15px 0;
    margin: 0;
    text-align: center;
    font-weight: 700;
  }

  @media screen and (max-width: 900px) {
    section {
      flex-direction: column;
      margin: 0px;
    }

    .pictures {
      width: 100%;
    }

    .picture--big {
      border-radius: 0px;
      object-fit: cover;
      height: 300px;
    }

    .thumbnails {
      display: none;
    }

    .text {
      width: 90%;
      margin-left: 0px;
    }

    .cart {
      flex-direction: column;
    }

    .num {
      width:100%;
    }

    .cart__btn {
      width:100%;
      margin-top: 20px;
    }
  }
</style>
