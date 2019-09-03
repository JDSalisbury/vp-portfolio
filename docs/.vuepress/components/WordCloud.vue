<template>
  <div style="height: 300px;" id="cloud">
    <!-- <img src="images/banner-three.jpg" alt /> -->
    <div v-if="cloudset">
      <wordcloud
        style="height: 300px;"
        id="test"
        :data="defaultWords"
        nameKey="lang"
        valueKey="lines"
        :color="myColors"
        :showTooltip="true"
      ></wordcloud>
    </div>
  </div>
</template>

<style>
#cloud {
  background-image: url("../public/images/banner-two.jpg");
}
</style>


<script>
import wordcloud from "vue-wordcloud";
import axios from "axios";

export default {
  name: "app",
  components: {
    wordcloud
  },
  async created() {
    let config = {
      headers: {
        authorization: "token b85774e88ae0d9e9b7965c290f26e89cdecf261f"
      }
    };
    await axios
      .get("https://api.github.com/users/jdsalisbury/repos?per_page=10", config)
      .then(response => {
        response.data.forEach(element => {
          axios.get(`${element.languages_url}`, config).then(response => {
            for (let [key, value] of Object.entries(response.data)) {
              if (
                this.defaultWords.length > 0 &&
                this.defaultWords.filter(e => e.lang == key).length > 0
              ) {
                this.defaultWords.filter(e => {
                  e.lang == key ? (e.lines += value) : "";
                });
              } else {
                this.defaultWords.push({ lang: key, lines: value });
              }
            }
            this.cloudset = true;
          });
        });
      });
  },
  data() {
    return {
      cloudset: false,
      myColors: ["#1f77b4", "#629fc9", "#94bedb", "#c9e0ef"],
      defaultWords: []
    };
  }
};
</script>