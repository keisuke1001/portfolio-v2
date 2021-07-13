<template>
  <div>
    <header>
      <div class="header">
        <NuxtLink to="/">
          <h1 class="logo">
            <img class="logoImg" src="/images/logo.svg" alt="" />
          </h1>
        </NuxtLink>

        <div
          class="ham-btn"
          :class="{ active: isMenu }"
          @click="isMenu = !isMenu"
        >
          <span class="h-line"></span>
        </div>
      </div>
      <nav class="g_Nav" :class="{ active: isMenu }" v-if="isMenu">
        <ul class="local_link">
          <li @click="isMenu = !isMenu" class="mNav_item">
            <nuxt-link to="/"> TOP</nuxt-link>
          </li>
          <li @click="isMenu = !isMenu" class="mNav_item">
            <nuxt-link to="/#works"> WORKS </nuxt-link>
          </li>
          <li @click="isMenu = !isMenu" class="mNav_item">
            <nuxt-link to="/#about"> ABOUT </nuxt-link>
          </li>
        </ul>
      </nav>
    </header>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isMenu: false,
    };
  },
};
</script>
<style scoped>
.header {
  display: flex;
  box-sizing: border-box;
  align-items: center;
  justify-content: space-between;
  max-width: 1000px;
  margin: 0 auto;
  padding: 30px 10px 0 10px;
}

.g_Nav {
  position: fixed;
  background-color: #445eed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 10;
  display: flex;
  visibility: hidden;
  justify-content: center;
  align-items: center;
  opacity: 0;
}
.active {
  opacity: 1;
  visibility: visible;
}

.local_link {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.mNav_item {
  margin-bottom: 30px;
}
.mNav_item a {
  color: #fff;
  font-size: 1.6rem;
  font-family: "Noto Sans JP", sans-serif;
  font-weight: 400;
}

.ham-btn {
  cursor: pointer;
}
.h-line,
.h-line::after,
.h-line::before {
  display: inline-block;
  content: "";
  width: 30px;
  height: 3px;
  border-radius: 3px;
  background-color: #333;
  z-index: 100;
  position: relative;
}
.h-line::after {
  position: absolute;
  transform: translateY(8px);
}
.h-line::before {
  position: absolute;
  transform: translateY(-8px);
}

.active .h-line {
  background-color: transparent;
}
.active .h-line::after {
  background-color: #fff;
  transform: rotate(-45deg);
  transition: 0.4s ease;
}
.active .h-line::before {
  background-color: #fff;
  transform: rotate(45deg);
  transition: 0.4s ease;
}

.logoImg {
  height: 24px;
  margin-left: -6px;
}
@media screen and (min-width: 768px) {
  .header {
    padding: 30px 0 0 0;
  }
}
</style>
