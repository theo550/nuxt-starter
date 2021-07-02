<template>
  <nav>
    <ul>
      <NuxtLink class="link" to="/"><li>accueil</li></NuxtLink>
      <NuxtLink class="link" to="/produits"><li>nos produits</li></NuxtLink>
      <NuxtLink class="link" to="/contact"><li>contact</li></NuxtLink>
      <NuxtLink class="link" to="/about"><li>à propos</li></NuxtLink>
    </ul>
  </nav>
</template>

<script>
export default {
  setup() {
    
  },
}
</script>

<style scoped>

  ul{
    display: flex;
    justify-content: flex-end;

    padding-right: 50px;

    margin: 30px 0;
  }

  .link{
    list-style: none;
    margin: 0 20px;

    cursor: pointer;

    color: black;
    text-decoration: none;
    text-transform: uppercase;
    font-size: 15px;
    font-weight: 300;

    position: relative;
  }

  .link::after{
    content: '';

    position: absolute;

    width: 100%;
    height: 2px;

    background: rgba(0, 0, 0, .5);

    left: 0;
    top: 25px;

    transform: scaleX(0);
    transition: transform .4s ease-out;
    transform-origin: right;
  }

  .link:hover::after{
    transform: scaleX(1);
    transition: transform .4s ease-out;
    transform-origin: left;
  }

</style>