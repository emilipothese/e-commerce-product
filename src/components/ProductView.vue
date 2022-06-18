<template>
  <section>
    <small>Sneaker Compagny</small>
    <h1>Fall limited edition sneakers</h1>
    <p class="description">These low-profile sneakers are your perfect casual wear
companion. Featuring a durable rubber outer sole, they'll
withstand everything the weather can offer.</p>
    <p class="description__price">$125.00 <span class="description__pourcentage">50%</span></p>
    <p class="description__price--sold">$250</p>
  </section>
</template>


<style scoped>
  h1 {
    text-transform: capitalize;
    font-weight: 900;
    font-size: 2.5rem;
    margin-top: 10px;
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
  }
</style>
