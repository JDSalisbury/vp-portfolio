<template>
  <div>
    <div class="avatar-div">
      <img class="avatar" src="../public/images/noodz.jpg" />
    </div>
    <div class="card">
      <div class="bio">
        <div class="head">
          <span>Software Developer</span>
        </div>
        <div class="info">
          <span>React/Redux | Vue/Vuex | Python/Django</span>
        </div>
        <div class="summary">
          <p>Software developer, with excellent interpersonal skills, outstanding work ethic, and proof-based problem-solving capabilities. Recognized team player seeking to leverage knowledge to help companies become more efficient in their technological efforts.</p>
        </div>
      </div>
      <div class="interests">
        <span>Interests: Guitar, MTG, Pokemon, Food</span>
      </div>
      <div class="banner"></div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style >
.avatar-div {
  position: relative;
  z-index: 1;
  display: flex;
  justify-content: center;
}
.avatar {
  display: block;
  width: 150px;
  height: auto;
  max-width: 150px;
  border-radius: 500rem;
}

.card {
  max-width: 600px;
  width: 100%;
  position: relative;
  top: -75px;
  padding-top: 75px;
  margin-left: auto;
  margin-right: auto;
  background: #fff;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  border-radius: 0.3rem;
  text-align: center;
}

.bio {
  padding: 1em;
}
.head {
  font-weight: 700;
  font-size: 1.3em;
}

.info {
  padding-top: 0.5rem;
  font-size: 1em;
  color: rgba(0, 0, 0, 0.4);
}

.summary {
  text-align: left;
}

.summary p {
  padding: 0.8em 0.5em 0;
  line-height: normal;
  -webkit-margin-before: 0em;
  -webkit-margin-after: 0em;
}

.interests {
  padding: 1em 1.5em;
  border-top: 1px solid rgba(34, 36, 38, 0.1);
}

.banner {
  background-image: url("../public/images/space-banner.jpg");
  padding: 1em 1.5em;
  border-top: 1px solid rgba(34, 36, 38, 0.1);
}
</style>