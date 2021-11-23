<template>
  <div class="wrap-get">
    <div class="container">
      <div class="row jcc">
        <p>get in <span>touch</span></p>
      </div>
      <div class="row content">
        <GITInfo />
        <GITForm />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {};
  },
};
</script>
<style lang="scss" scoped>
.wrap-get {
  padding-bottom: 90px;
}
p {
  text-transform: capitalize;
  font-weight: bold;
  padding: 90px 0 70px;
  text-align: center;
  line-height: 30px;
  font-size: 30px;
    color: var(--title-text);
}
span {
  color: var(--maincolor);
}
.jcc {
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 1;
}
.content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  padding: 0 15px;
}
@media (max-width: 1263px) {
  .content {
    flex-direction: column-reverse;
  }
}
</style>