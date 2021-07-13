<template>
  <div>
    <footer class="footer">
      <div class="fText">
        <h3 class="flogo">
          <a href="#">
            <img class="logoImg" src="/images/logo.svg" alt="" />
          </a>
        </h3>
        <span class="copy"><small>&copy;Keisuke</small></span>
      </div>
      <div class="pageTop" @click="pageTop">
        <img class="topImg" src="/images/icon-page-top.svg" alt="" />
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  methods: {
    pageTop() {
      window.scrollTo({
        top: 0,
        behavior: "smooth",
      });
    },
  },
};
</script>
<style scoped>
.footer {
  display: flex;
  max-width: 1000px;
  justify-content: space-between;
  align-items: center;
  margin: 0 auto;
  padding: 60px 10px 20px 10px;
}
.logoImg {
  height: 24px;
  margin-left: -6px;
}
.topImg {
  height: 42px;
  margin-left: 20px;
}
small {
  font-family: "Nunito", sans-serif;
  font-weight: 300;
}
@media screen and (min-width: 768px) {
  .footer {
    padding: 60px 0px 20px 0px;
  }
}
</style>
