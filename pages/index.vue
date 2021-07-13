<template>
  <div>
    <Header />
    <main>
      <h2 id="works">WORKS</h2>
      <section class="workWrap">
        <article
          v-for="content in contents"
          :key="content.id"
          class="workItems"
        >
          <nuxt-link :to="`/${content.id}`">
            <div class="card">
              <img :src="content.thumbnail.url" alt="" />
              <h3 class="itemName">{{ content.title }}</h3>
            </div>
          </nuxt-link>
        </article>
      </section>
    </main>
    <Profile id="about" />
    <Footer />
  </div>
</template>
<script>
import Header from "@/components/Header.vue";
import Profile from "@/components/Profile.vue";
import Footer from "@/components/Footer.vue";
import axios from "axios";
export default {
  async asyncData() {
    const { data } = await axios.get(
      "https://keisuke.microcms.io/api/v1/portfolio",
      {
        headers: { "X-API-KEY": process.env.API_KEY },
      }
    );
    return data;
  },
  mounted() {
    const hash = this.$route.hash;
  },
};
</script>
<style>
h2 {
  color: #333;
  font-size: 34px;
  text-align: center;
  padding: 60px 0;
  font-family: "Nunito", sans-serif;
  font-weight: 600;
}
main {
  max-width: 1000px;
  margin: 0 auto;
}
.workWrap {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  justify-content: center;
  gap: 40px;
  padding: 10px;
}

.card img {
  border: 1px solid #ddd;
}
img {
  width: 100%;
  height: auto;
}
.itemName {
  color: #333;
  font-size: 14px;
  font-family: "Noto Sans JP", sans-serif;
  font-weight: 400;
  padding-top: 10px;
}
</style>
