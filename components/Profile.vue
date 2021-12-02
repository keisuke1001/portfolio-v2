<template>
  <div>
    <h2>ABOUT</h2>
    <section class="prof">
      <img class="prfImg" src="/images/icon-prof.jpg" alt="" />
      <p class="name">多田 圭助</p>
      <div class="profText">
        <p>
          2000年10月生まれ。富山県出身。日本工学院専門学校 Webクリエイター科
        </p>
        <p>ゲームとラーメンが好き</p>
        <p>HTML5 / CSS / SCSS / javascript / WordPress / Nuxt.js / Vue.js / Tailwind / Adobe XD / Figma / Illustrator / Photshop /</p>
      </div>
      <div class="link">
        <a href="https://github.com/keisuke1001">
          <div class="github">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="16"
              height="16"
              viewBox="0 0 16 16"
            >
              <path
                id="mark-github"
                d="M8,0A8.1,8.1,0,0,0,0,8.2a8.181,8.181,0,0,0,5.47,7.782c.4.072.55-.174.55-.39,0-.195-.01-.841-.01-1.528-2.01.379-2.53-.5-2.69-.964a2.982,2.982,0,0,0-.82-1.159c-.28-.154-.68-.533-.01-.543a1.6,1.6,0,0,1,1.23.841,1.686,1.686,0,0,0,2.33.677,1.742,1.742,0,0,1,.51-1.1c-1.78-.205-3.64-.913-3.64-4.05a3.238,3.238,0,0,1,.82-2.2,3.017,3.017,0,0,1,.08-2.174s.67-.215,2.2.841a7.363,7.363,0,0,1,4,0c1.53-1.066,2.2-.841,2.2-.841a3.017,3.017,0,0,1,.08,2.174,3.219,3.219,0,0,1,.82,2.2c0,3.148-1.87,3.845-3.65,4.05a1.969,1.969,0,0,1,.54,1.517c0,1.1-.01,1.979-.01,2.256,0,.215.15.472.55.39A8.2,8.2,0,0,0,16,8.2,8.1,8.1,0,0,0,8,0Z"
                fill-rule="evenodd"
              />
            </svg>
            <span>GitHub</span>
          </div>
        </a>
        <a href="mailto:k019g1393@g.neec.ac.jp">
          <div class="email">
            <svg
              id="email_black_24dp"
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24"
            >
              <path
                id="email1"
                data-name="email"
                d="M0,0H24V24H0Z"
                fill="none"
              />
              <path
                id="email2"
                data-name="email2"
                d="M22,6a2.006,2.006,0,0,0-2-2H4A2.006,2.006,0,0,0,2,6V18a2.006,2.006,0,0,0,2,2H20a2.006,2.006,0,0,0,2-2ZM20,6l-8,5L4,6Zm0,12H4V8l8,5,8-5Z"
              />
            </svg>
            <span>E-Mail</span>
          </div>
        </a>
      </div>
    </section>
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
.prof {
  display: grid;
  justify-content: center;
  justify-items: center;
  gap: 30px;
  padding: 0 10px 0 10px;
}
.prfImg {
  width: 250px;
  height: auto;
}
.name {
  font-size: 24px;
  font-family: "Noto Sans JP", sans-serif;
}
.profText p {
  color: #333;
  text-align: center;
  line-height: 24px;
  font-weight: 300;
  font-family: "Noto Sans JP", sans-serif;
}
.link {
  display: flex;
  align-items: center;
  column-gap: 30px;
}
.github,
.email {
  display: flex;
  align-items: center;
  column-gap: 10px;
}
.github span,
.email span {
  color: #333;
  font-weight: 300;
  font-family: "Noto Sans JP", sans-serif;
}
.github svg {
  color: #333;
  height: 18px;
  width: auto;
}
@media screen and (min-width: 768px) {
  .prof {
    padding: 0;
  }
}
</style>
