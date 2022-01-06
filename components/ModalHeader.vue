<template>
  <div class="modal-wrapper">
    <div class="bg"></div>
    <div class="modal-content">
      <div class="row text">
        <p>your video</p>
        <span @click="$emit('openModal1')"><fa icon="window-close" /></span>
      </div>
      <div class="row video">
        <iframe
          src="https://www.youtube.com/embed/pH6WoGSEZUo"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.modal-wrapper {
  position: fixed;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba($color: #000000, $alpha: 0.7);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 9999;
  .modal-content {
    padding: 10px 20px;
    max-width: 1000px;
    width: 100%;
    height: 540px;
    background-color: #000000;
  }
  .text {
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: black;
    border-bottom: 1px solid black;
    padding: 15px;
    p {
      margin-bottom: 10px;
      text-transform: capitalize;
      color: white;
    }
    span {
      color: white;
      cursor: pointer;
    }
  }
  .video {
    max-width: 1000px;
    max-height: 450px;
    width: 100%;
    height: 100%;
    iframe {
      width: 100%;
    }
  }
}
</style>
