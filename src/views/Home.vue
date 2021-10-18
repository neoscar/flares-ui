<template>
  <div>
    <!-- 导航条 -->
    <Topnav />
    <!-- 内容区 -->
    <div class="banner">
      <!-- 标题 -->
      <h1>flares-ui</h1>
      <h2>一个厉害的 UI 框架</h2>
      <!-- 链接 -->
      <p class="actions">
        <a href="#">Github</a>
        <a href="#">开始</a>
      </p>
    </div>
  </div>
</template>
<script lang="ts">
import Topnav from '../components/Topnav.vue'
export default {
  components: {
    Topnav
  }
}
</script>
