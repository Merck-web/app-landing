<template>
  <div class="facts-wrapper">
    <h1>fun <span>facts</span></h1>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam non quidem
      sed libero, similique quam ex tenetur repellat molestiae mollitia
      nesciunt, quasi odit fuga ut eveniet, pariatur corrupti dolorem natus?
    </p>
    <div class="cardBox">
      <GridFacts />
    </div>
  </div>
</template>
<style lang="scss" scoped>
.facts-wrapper {
  h1 {
    padding-bottom: 40px;
    text-transform: capitalize;
    span{
        color: var(--maincolor);
    }
  }
  p {
    padding-bottom: 50px;
    color: var(--black-400);
  }
}
</style>