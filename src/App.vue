<template>
  <div>导航栏</div>
  <router-link to="/">Frank</router-link> |
  <router-link to="/xxx">Frank2</router-link>
  <hr />
  <router-view />
</template>

<script>
export default {
  name: 'App'
}
</script>
