<template>
  <div class="wrap-form">
    <div class="input-box">
      <div class="row">
        <input v-model="name" type="text" placeholder="Your Name" />
        <input v-model="Email" type="mail" placeholder="Your E-mail" />
      </div>
      <div class="row">
        <input v-model="Phone" type="tell" placeholder="Your Phone" />
      </div>
      <div class="row">
        <input v-model="Subject" type="text" placeholder="Your Subject" />
      </div>
      <div class="row">
        <textarea v-model="Message" placeholder="Your Message"></textarea>
      </div>
    </div>
    <div class="btn">
      <button type="submit">send message</button>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: "",
      Email: "",
      Phone: "",
      Subject: "",
      Message: "",
    };
  },
};
</script>
<style lang="scss" scoped>
.wrap-form {
  padding-top: 10px;
  .row {
    padding-bottom: 25px;
  }
  .row:nth-child(1) {
    input + input {
      margin-left: 30px;
    }
    input {
      width: 350px;
    }
  }
  .row:nth-child(2),
  .row:nth-child(3),
  .row:nth-child(4) {
    width: calc(100% + 25px);
    input {
      width: calc(100% + 25px);
    }
    textarea {
      width: calc(100% + 25px);
      height: 140px;
      resize: none;
    }
  }
  .input-box {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    flex-direction: column;
    input {
      padding: 10px 25px;
      line-height: 35px;
      background-color: var(--black-000);
      color: var(--black-400);
      box-shadow: var(--shadow-black-300);
      outline: none;
    }
    textarea {
      padding: 10px 25px;
      line-height: 25px;
      background-color: var(--black-000);
      color: var(--black-400);
      box-shadow: var(--shadow-black-300);
      outline: none;
    }
  }
  .btn {
    margin-top: 30px;
    background-color: var(--maincolor);
    color: white;
    max-width: 200px;
    text-align: center;
    width: 100%;
    padding: 20px 30px;
    border-radius: 50px;
    button {
      text-transform: capitalize;
      font-size: 16px;
      font-weight: 600;
      box-shadow: none;
    }
  }
}
@media (max-width: 929px) {
  .row:nth-child(1) {
    display: block;
    width: calc(100% + 25px) !important;
    input {
      width: 100% !important;
    }
    input + input {
      margin-left: 0 !important;
      margin-top: 25px;
    }
  }
  .wrap-form {
    margin-bottom: 30px;
  }
}
</style>