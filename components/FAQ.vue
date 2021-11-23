<template>
    <div class="wrap-faq">
          <div class="container">
    <div class="row jcc">
      <p>freeqently <span>asked</span> queries</p>
    </div>
    <div class="row">
        <FAQAccordeon />
    </div>
  </div>
    </div>
</template>
<script>
export default {
  data() {
    return {
    };
  },
};
</script>
<style lang="scss" scoped>
.wrap-faq {
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
</style>