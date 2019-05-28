<template>
  <div id="app">
    <!-- keep-alive缓存，detail不做缓存 -->
    <keep-alive exclude="Detail">
    <router-view/>
    </keep-alive>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
</style>
