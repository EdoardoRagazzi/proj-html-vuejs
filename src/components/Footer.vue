<template>
  <div class="footer">
    <div class="tabs d-flex justify-content-around">
      <div class="col">
        <img src="..\assets\img\theme_eduprime_logo.png" alt="" />
        <div class="text">
          <p>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit.
            Praesentium consequuntur similique fuga commodi quidem neque harum
            dignissimos minima dolorum quam.
          </p>
          <div class="icons">
            <div class="icon">
              <i class="bi bi-facebook"></i>
            </div>
            <div class="icon">
              <i class="bi bi-linkedin"></i>
            </div>
            <div class="icon">
              <i class="bi bi-twitter"></i>
            </div>
          </div>
        </div>
      </div>
      <div class="col">
        <ul>
          <h4>Get Edu Prime</h4>
          <li v-for="(dc, index) in Dc" :key="index">
            <a :href="dc.url">{{ dc.text }}</a>
          </li>
        </ul>
      </div>
      <div class="col">
        <ul>
          <h4>Networking</h4>
          <li v-for="(dc, index) in Dc" :key="index">
            <a :href="dc.url">{{ dc.text }}</a>
          </li>
        </ul>
      </div>
      <div class="col last">
        <div class="input">
          <input type="text" placeholder="Search..." />
          <button type="submit">
            <i class="bi bi-search"></i>
          </button>
        </div>
        <div class="text">
          <h5>Search Categories</h5>
        </div>
        <div class="buttons">
          <button class="btn">Search</button>
          <button class="btn">Search</button>
          <button class="btn">Search</button>
          <button class="btn">Search</button>
          <button class="btn">Search</button>
          <button class="btn">Search</button>
        </div>
        <div class="sign">
          <h5>Edoardo Ragazzi</h5>
          <p>.All rights reserved</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import listaDc from "@/data/listaDc.js";
export default {
  name: "Footer",
  data() {
    return {
      Dc: listaDc,
    };
  },
};
</script>

<style scoped lang="scss">
@import "@/style/common.scss";
.footer {
  height: 700px;
  background-color: #e56768;
}
.text p {
  color: white;
  text-align: left;
  margin: 20px;
}
.tabs {
  width: 85%;
  margin: auto;
  .col {
    margin-top: 200px;
    text-align: left;
    h4 {
      font-weight: 900;
      color: white;
      font-family: "Fredoka One";
    }
    ul {
      list-style: none;
      li {
        text-align: left;
        line-height: 30px;
        a {
          text-decoration-line: none;
          color: white;
          text-align: left;
        }
      }
    }
  }
  img {
    height: 60px;
    max-width: 270px;
  }
  .icon {
    display: inline-block;
    height: 50px;
    width: 50px;
    border-radius: 50%;
    border: 2px solid #e9d758;
    vertical-align: middle;
    line-height: 48px;
    margin: 10px;

    i {
      padding: 15px;
      font-size: 1em;
      color: white;
    }
    &:hover {
      cursor: pointer;
      background-color: #e9d758;
    }
  }
}
.input {
  position: relative;

  i {
    font-size: 1em;
    font-weight: 400;
  }
  input {
    border-radius: 35px;
    height: 70px;
    font-size: 15px;
    border: 0 none;
    float: left;
    padding: 25px;
    width: 300px;
    font-weight: 400;
    outline: 0;
  }
  button {
    position: absolute;
    top: 0;
    height: 70px;
    padding: 21px 28px;
    background: #e9d758;
    border-radius: 50%;
    right: 10px;
    color: #fff;
    font-size: 20px;
    box-shadow: none;
    border: 0;
    outline: 0;
    box-shadow: 0px 0px 20px rgb(0 0 0 / 7%);
    transition: all 300ms ease;
    -webkit-transition: all 300ms ease;
    &:hover {
      background-color: #e56768;
    }
  }
}
.last {
  .text {
    padding-top: 50px;
    margin-top: 100px;
    text-align: right;
    color: white;
  }
  .buttons {
    padding: 20px;
    width: 100%;
    .btn {
      font-size: 0.5em;
      border: 1px solid white;
      color: white;
      height: 30px;
      margin: 2px;
      text-transform: uppercase !important;
      border-radius: 50px;
      letter-spacing: 0.5px;
      text-align: center;
      transition: all 300ms ease;
      -webkit-transition: all 300ms ease;
      &:hover {
        background-color: #e9d758;
      }
    }
  }
}
.sign {
  color: #e9d758;
  font-size: 15px;
  font-weight: 600;
  font-family: "Fredoka One";
  text-align: right;
  p {
    font-size: 10px;
  }
}
</style>