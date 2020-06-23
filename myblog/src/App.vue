<template>
  <div id="app">
    <h1>Welcome youao's Blog</h1>
    <p><a href="https://github.com/youao/blog">Read more</a> about this blog.</p>
    <div class="websites">
      <a v-for="(item, index) in webs" :key="index" :href="item.link" :title="item.title">
        <img :src="item.img">
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      webs: [{
        title: "github",
        img: "https://github.githubassets.com/pinned-octocat.svg",
        link: "https://github.com/youao"
      }, {
        title: "掘金",
        img: "https://b-gold-cdn.xitu.io/favicons/v2/safari-pinned-tab.svg",
        link: "https://juejin.im/user/5d9c77f351882509165fee81/posts"
      }]
    };
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: auto;
}
h1 {
  margin-top: 200px;
  margin-bottom: 20px;
  font-size: 50px;
}
a {
  color: #42b983;
}
.websites img {
  width: 22px; height: 22px;
  margin: 20px;
}
</style>
