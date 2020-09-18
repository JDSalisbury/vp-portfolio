<template>
  <div>
    <div class="me-div">
      <img class="me" src="../public/images/detroit.jpg" />
    </div>
    <br />
  </div>
</template>

<script>
export default {};
</script>

<style>
.me-div {
  position: relative;
  z-index: 1;
  display: flex;
  justify-content: center;
  margin-top: 50px;
}
.me {
  display: block;
  /* width: 475px; */
  /* height: 100%; */
  /* max-width: 150px; */
  border-radius: 2rem;
  box-shadow: 20px 14px 20px 0px #adadad;
}
</style>
