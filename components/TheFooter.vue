<template>
  <div class="footer">
    <div class="container">
      <div class="contacts">
        <div class="about">
          <div class="title">
            <p>about us</p>
          </div>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam
            recusandae amet eius dicta distinctio soluta voluptatibus ut, hic
            aut molestiae omnis, inventore obcaecati neque vel similique
            excepturi illum, sunt velit.
          </p>
        </div>
        <div class="company">
          <div class="title">
            <p>company</p>
          </div>
          <ul>
            <li>privacy policy</li>
            <li>terms and condition</li>
            <li>latest blogs</li>
            <li>app services</li>
          </ul>
        </div>
        <div class="quick">
          <div class="title">
            <p>quick links</p>
          </div>
          <ul>
            <li>home</li>
            <li>features</li>
            <li>screenshots</li>
            <li>picing</li>
            <li>testimonials</li>
          </ul>
        </div>
        <div class="social">
          <div class="title">
            <p>social pages</p>
          </div>
          <ul>
            <li>facebook</li>
            <li>twitter</li>
            <li>instagram</li>
            <li>linkedin</li>
          </ul>
        </div>
      </div>
      <p class="copy">&#169;2021 @ my client</p>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.footer {
  background-color: var(--maincolor);
  .contacts {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    padding-top: 60px;
    padding-bottom: 60px;
    color: white;
    text-transform: capitalize;
    border-bottom: 1px solid white;
    .about {
      max-width: 250px;
      .title {
        p {
          text-transform: capitalize;
        }
      }
      p {
        text-transform: none;
        line-height: 25px;
      }
    }
    .title {
      font-size: 18px;
      font-weight: 600;
      padding-bottom: 40px;
    }
    li {
      padding-bottom: 10px;
      cursor: pointer;
      transition: var(--transition);
    }
    li:hover {
      color: var(--color-3);
      transition: var(--transition);
    }
  }
  .copy {
    color: white;
    text-align: center;
    text-transform: capitalize;
    font-size: 18px;
    line-height: 18px;
    padding: 25px 0;
  }
}
@media (max-width: 800px) {
  .contacts {
    flex-direction: column;
    align-items: flex-start !important;
    text-align: left;
    padding: 0 20px;
    .about {
      max-width: none !important;
      margin-bottom: 20px;
    }
    .company,
    .quick,
    .social {
      width: 200px;
      margin-bottom: 20px;
    }
    .social {
      margin-bottom: 0;
    }
    .title {
      padding-bottom: 20px !important;
    }
  }
}
</style>