<template>
  <div>
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
