<template>
  <div>
    <header>
      <h2><nuxt-link to="/about">NuxStore About Us</nuxt-link></h2>
      <nav>
        <ul>
          <li>
            <nuxt-link to="/">Home</nuxt-link>
          </li>
          <li><nuxt-link to="/about">About</nuxt-link></li>
          <li><nuxt-link to="/products">Products</nuxt-link></li>
        </ul>
      </nav>
    </header>

    <!-- output page content -->
    <div>
      <slot />
      <!-- this is like @yield -->
    </div>
  </div>
</template>

<style>
.router-link-exact-active {
  color: #195d58;
}
</style>
