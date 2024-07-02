<template>
  <header class="main-header">
    <div class="left-header">
      <h1>MORENT</h1>
      <label class="header-search">
        <img src="/public/icons/header/search-normal.svg" alt="" />
        <input type="text" placeholder="Search something here" />
      </label>
    </div>
    <div class="right-header">
      <div class="header-circle">
        <img src="/public/icons/header/heart.svg" alt="" />
      </div>
      <div class="header-circle">
        <img src="/public/icons/header/notification.svg" alt="" />
      </div>
      <div class="header-circle">
        <img src="/public/icons/header/settings.svg" alt="" />
      </div>
      <div class="header-circle">
        <img src="/public/icons/header/account.svg" alt="" />
      </div>
    </div>
  </header>
</template>

<style lang="scss">
.main-header {
  background-color: #ffffff;
  height: 124px;
  border: 1px solid #c3d4e9;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 64px;

  * {
    background-color: #ffffff;
  }

  .left-header {
    display: flex;
    h1 {
      cursor: pointer;
      color: #3563e9;
      margin: 0;
    }

    .header-search {
      margin-left: 64px;

      img {
        position: absolute;
        margin-left: 20px;
        margin-top: 10px;
      }
      input {
        width: 492px;
        height: 44px;
        padding-left: 64px;
        border: 1px solid #c3d4e950;
        border-radius: 70px;
        transition: 0.2s;
      }
      input:focus {
        border: 1px solid #c3d4e9ff;
      }
    }
  }
  .right-header {
    display: flex;
    gap: 20px;
    .header-circle {
      cursor: pointer;
      height: 44px;
      width: 44px;
      border: 1px solid #c3d4e950;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      transition: 0.2s;
    }
    .header-circle:hover {
      border: 1px solid #c3d4e9ff;
    }
  }
}
</style>
