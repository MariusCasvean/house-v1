<template>
  <header>
    <div class="logo-container">
      <img src="../images/mc-logo.jpg" alt="Marrona logo" />
      Welcome {{ currentUser }}
    </div>
    <div class="nav-container">
      <div class="nav-item">
        <router-link to="/">Home</router-link>
      </div>
      <div class="nav-item">
        <router-link to="/about">About</router-link>
      </div>
    </div>
  </header>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Header",
  components: {},
  props: {
    currentUser: String,
  },
});
</script>

<style lang="scss" scoped>
header {
  background-color: #33d6ff;
  padding: 20px 60px;
  color: grey;
  text-transform: uppercase;
  display: flex;
  justify-content: space-between;
  align-items: center;
  .logo-container {
    img {
      height: 60px;
      width: 60px;
      border-radius: 50%;
    }
  }
  .nav-container {
    display: flex;
    align-items: center;
    // padding: 10px;
    // border: 1px solid red;
    .nav-item:not(:last-child) {
      margin-right: 60px;
    }
    .nav-item {
      font-weight: bold;
      a {
        color: black;
        text-decoration: none;
      }
      :hover {
        color: #21b1d4;
      }
    }
  }
}
</style>
