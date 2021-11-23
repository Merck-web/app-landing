<template>
  <div class="wrap-info">
    <div class="titile">
      <p>for any quires and support</p>
    </div>
    <div class="contact-section">
      <ul>
        <li>
          <div class="text-content">
            <p>company location</p>
            <p>{{ info1 }}</p>
          </div>
        </li>
        <li>
          <div class="text-content">
            <p>write to us at</p>
            <p>{{ info2 }}</p>
          </div>
        </li>
        <li>
          <div class="text-content">
            <p>call us on</p>
            <p>{{ info3 }}</p>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      info1: "199 xyz gali, New city",
      info2: "info@gmail.com",
      info3: "88005553555",
    };
  },
};
</script>
<style lang="scss" scoped>
.wrap-info {
  margin-top: -110px;
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  flex-direction: column;
  padding-left: 30px;
  .titile {
    text-transform: capitalize;
    font-size: 18px;
    font-weight: 600;
    padding-bottom: 50px;
      color: var(--title-text);
  }
  .text-content {
    position: relative;
    p:first-child {
      text-transform: capitalize;
      font-size: 16px;
      font-weight: 500;
        color: var(--title-text);
      padding-bottom: 10px;
    }
    p + p {
      font-size: 16px;
      color: var(--black-400);
      padding-bottom: 40px;
    }
  }
  .text-content::before {
    content: "";
    position: absolute;
    width: 40px;
    height: 40px;
    left: -52px;
    top: 6px;
    border-radius: 50%;
    border: 2px solid var(--maincolor);
  }
  .text-content::after {
    content: "";
    position: absolute;
    background-size: 35% 35%;
    filter: invert(42%) sepia(41%) saturate(7095%) hue-rotate(237deg)
      brightness(99%) contrast(103%);
    background-position: center;
    width: 40px;
    height: 40px;
    left: -52px;
    top: 6px;
  }
  li:nth-child(1) .text-content::after {
    background-image: url(../static/img/icons/location-arrow-solid.svg);
  }
  li:nth-child(2) .text-content::after {
    background-image: url(../static/img/icons/envelope-solid.svg);
  }
  li:nth-child(3) .text-content::after {
    background-image: url(../static/img/icons/phone-solid.svg);
  }
}
@media (max-width: 1263px) {
  .wrap-info {
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    align-items: flex-end;
    text-align: right;
    width: calc(100% - 120px);
      margin-top: 0;
      padding-left: 0;
  }
}
@media (max-width: 500px) {
  .wrap-info {
    width: 100%;
  }
}
</style>