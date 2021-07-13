<template>
  <div>
    <Header />
    <main class="main">
      <div class="slugtext">
        <h2 class="title">{{ title }}</h2>
        <a :href="gitlink" class="gitlink">{{ GitHub }}</a>
      </div>
      <div class="img_list">
        <img :src="img1.url" alt="" />
        <img :src="img2.url" alt="" />
        <img :src="img3.url" alt="" />
      </div>
    </main>
    <Footer />
  </div>
</template>

<script>
import axios from "axios";

export default {
  async asyncData({ params }) {
    const { data } = await axios.get(
      `https://keisuke.microcms.io/api/v1/portfolio/${params.slug}`,
      {
        headers: { "X-API-KEY": process.env.API_KEY },
      }
    );
    return data;
  },
};
</script>
<style scoped>
main {
  margin: 0 auto;
  max-width: 1000px;
}
.slugtext {
  padding: 60px 0 30px 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.slugtext h2 {
  color: #333;
  padding: 0;
  font-size: 34px;
  text-align: center;
  font-family: "Nunito", sans-serif;
  font-weight: 600;
}
.gitlink {
  display: inline-block;
  font-size: 16px;
  font-family: "Nunito", sans-serif;
  font-weight: 600;
  color: #fff;
  background-color: #445eed;
  padding: 10px 60px;
  transition: 0.3s;
}
.gitlink:hover {
  color: #445eed;
  background-color: transparent;
  border: solid 1px #445eed;
  padding: 10px 60px;
}
.gitlink:empty {
  display: none;
}
.img_list img {
  width: 100%;
  border: 1px solid #ddd;
  margin: 30px 0;
}
@media screen and (max-width: 767px) {
  .slugtext {
    display: block;
    padding: 0 10px;
  }
  .slugtext h2 {
    font-size: 24px;
    text-align-last: left;
    padding: 40px 0;
  }
  .img_list {
    padding: 0 10px;
  }
}
</style>
