<template>
  <section class="about-us">
    <div class="about">
      <img
        src="https://www.reiss.com/nxtcms/resource/blob/6204624/96c19bea7d48daa75f1583e76ff4d857/reiss-ww-uk-dresses-mb-data.jpg"
        class="pic"
      />
      <div class="text">
        <h2>About Us</h2>
        <h5>Lorem ipsum dolor & <span>Fashion Designer</span></h5>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Expedita
          natus ad sed harum itaque ullam enim quas, veniam accusantium, quia
          animi id eos adipisci iusto molestias asperiores explicabo cum vero
          atque amet corporis! Soluta illum facere consequuntur magni. Ullam
          dolorem repudiandae cumque voluptate consequatur consectetur, eos
          provident necessitatibus reiciendis corrupti!
        </p>
        <div class="data">
          <nuxt-link to="/#contact" class="hire"
            ><i class="fa-solid fa-phone"></i> Contact Us</nuxt-link
          >
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
definePageMeta({
  title: "NuxtStore | About Us",
  // layout: "about",
});
</script>

<style>
@import url("~/assets/css/about.css");
</style>
