<template>
  <footer class="main-footer">
    <div class="f-header">
      <div class="left">
        <h1>MORENT</h1>
        <p>Our vision is to provide convenience and help increase your sales business.</p>
      </div>
      <div class="right">
        <div class="links-block">
          <h2>About</h2>
          <p>How it works</p>
          <p>Featured</p>
          <p>Partnership</p>
          <p>Bussiness Relation</p>
        </div>
        <div class="links-block">
          <h2>Community</h2>
          <p>Events</p>
          <p>Blog</p>
          <p>Podcast</p>
          <p>Invite a friend</p>
        </div>
        <div class="links-block">
          <h2>Socials</h2>
          <p>Discord</p>
          <p>Instagram</p>
          <p>Twitter</p>
          <p>Facebook</p>
        </div>
      </div>
    </div>
    <hr />
    <div class="f-footer">
      <div class="rights">
        <h3>©2024 MORENT. All rights reserved</h3>
      </div>

      <div class="policies">
        <p>Privacy & Policy</p>
        <p>Terms & Condition</p>
      </div>
    </div>
  </footer>
</template>

<style lang="scss">
.main-footer {
  margin-top: 64px;
  height: 480px;
  display: flex;
  flex-direction: column;
  background-color: #ffffff;
  padding: 80px 4.44vw 60px 4.44vw;

  * {
    background-color: #ffffff;
  }

  .f-header {
    display: flex;
    justify-content: space-between;

    .left {
      h1 {
        font-size: 32px;
        color: #3563e9;
      }
      p {
        margin-top: 16px;
        font-size: 16px;
        color: #131313c2;
        width: 292px;
      }
    }
    .right {
      padding-right: 4.44vw;
      display: flex;
      gap: 60px;

      .links-block {
        display: flex;
        flex-direction: column;

        h2 {
          margin: 0;
          margin-bottom: 36px;
          font-size: 20px;
          color: #1a202c;
          font-weight: 500;
        }

        p {
          cursor: pointer;
          margin: 0;
          margin-bottom: 24px;
        }
      }
    }
  }

  hr {
    margin-top: 16px;
  }

  .f-footer {
    display: flex;
    margin-top: 48px;
    align-items: center;
    justify-content: space-between;

    .rights {
      h3 {
        color: #1a202c;
        font-size: 16px;
      }
    }

    .policies {
      display: flex;
      gap: 64px;

      p {
        cursor: pointer;
      }
    }
  }
}
</style>
