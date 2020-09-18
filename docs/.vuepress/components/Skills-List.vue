<template>
  <div class="stats">
    <div class="stat">
      <div class="png-bg">
        <img class="png" :src="$withBase(`/images/python.png`)" />
      </div>
      <span></span>
      <progress max="100" value="85"></progress>
    </div>

    <div class="stat">
      <div class="png-bg">
        <img class="png" :src="$withBase(`/images/react.png`)" />
      </div>
      <span></span>
      <progress max="100" value="75"></progress>
    </div>

    <div class="stat">
      <div class="png-bg">
        <img class="png" :src="$withBase(`/images/vue.png`)" />
      </div>
      <span></span>
      <progress max="100" value="80"></progress>
    </div>

    <div class="stat">
      <div class="png-bg">
        <img class="png" :src="$withBase(`/images/docker.png`)" />
      </div>
      <span></span>
      <progress max="100" value="63"></progress>
    </div>

    <div class="stat">
      <div class="png-bg">
        <img class="png" :src="$withBase(`/images/java.png`)" />
      </div>
      <span></span>
      <progress max="100" value="30"></progress>
    </div>

    <div class="stat">
      <div class="png-bg">
        <img class="png" :src="$withBase(`/images/php.png`)" />
      </div>
      <span></span>
      <progress max="100" value="40"></progress>
    </div>

    <div class="stat">
      <div class="png-bg">
        <img class="png" :src="$withBase(`/images/jenkins.png`)" />
      </div>
      <span></span>
      <progress max="100" value="55"></progress>
    </div>

    <div class="stat" @click="set_true('aws')">
      <div class="png-bg">
        <img class="png" :src="$withBase(`/images/aws.png`)" />
      </div>
      <span></span>
      <progress max="100" value="50"></progress>
      <div v-if="aws">AWS Stuff</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      python: false,
      react: false,
      vue: false,
      java: false,
      php: false,
      docker: false,
      jenkins: false,
      aws: false
    };
  },
  methods: {
    set_true(data_set) {
      this[data_set] = !this[data_set];
      console.log('Clicked', data_set);
    }
  }
};
</script>

<style scoped>
progress[value] {
  width: 60%;
  height: 30px;
}
.stats {
  display: flex;
  justify-content: center;
  flex-direction: column;
}
.stat {
  display: flex;
  justify-content: center;
  align-items: center;
}
.png-bg {
  /* background-color: #bfd9f9a3; */
  width: 70px;
  height: 40px;
  border-radius: 70px;
  z-index: 1;
  display: flex;
  justify-content: center;
}
.png {
  position: absolute;
  width: 40px;
  z-index: 1;
}
span {
  padding: 3px;
}
</style>
