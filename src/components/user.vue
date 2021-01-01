<template>
  <div class="user">
    <div class="left">
      <div class="userHead">
        <img src="../assets/images/wxy.jpg" alt="" />
      </div>
      <ul>
        <li>
          <div>总分</div>
          <div>0</div>
        </li>
        <li>
          <div>6元</div>
          <div>0</div>
        </li>
        <li>
          <div>3元</div>
          <div>0</div>
        </li>
        <li>
          <div>1元</div>
          <div>0</div>
        </li>
      </ul>
    </div>
    <div class="right">
      <ul>
        <li>
          <img src="../assets/images/hczz.jpg" alt="" />
        </li>
        <li>
          <img src="../assets/images/hczz.jpg" alt="" />
        </li>
        <li>
          <img src="../assets/images/hczz.jpg" alt="" />
        </li>
        <li>
          <img src="../assets/images/hczz.jpg" alt="" />
        </li>
      </ul>
      <div class="bottom">
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
        <li class="box"><img src="../assets/images/Q.jpg" alt="" /></li>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "user",
  props: {
    msg: String,
  },
  mounted() {},
  methods: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.user {
  flex: 1;
  display: flex;

  .left {
    width: 20%;
    height: 100%;
    display: flex;
    flex-direction: column;
    .userHead {
      width: 100px;
      height: 100px;
      margin: 15px auto;
      border: 1px solid black;

      img {
        width: 100%;
        height: 100%;
      }
    }
    ul {
      width: 100px;
      border: 1px solid black;
      flex: 1;
      margin: 0 auto;
      margin-bottom: 15px;
      display: flex;
      flex-direction: column;

      li {
        flex: 1;
        display: flex;

        div {
          flex: 1;
          border-top: 1px solid black;
          display: flex;
          align-items: center;
          justify-content: center;
        }
        div:nth-child(1) {
          border-right: 1px solid black;
        }
      }
      li:nth-child(1) div {
        border-top: none;
      }
    }
  }
  .right {
    // flex: 1;
    width: 80%;
    background: pink;
    display: flex;
    flex-direction: column;

    ul {
      width: 100%;
      height: 100px;
      display: flex;
      justify-content: space-around;
      align-items: center;
      margin: 0;
      li {
        width: 22%;
        height: 70px;
        border: 1px solid black;
        transition: 0.1s;
        img {
          width: 100%;
          height: 100%;
        }
      }
      li:hover {
        width: 33%;
        height: 100px;
      }
    }
    .bottom {
      flex: 1;
      background: green;
      overflow-x: scroll;
      /*添加横向滚动条*/
      white-space: nowrap;
      /*不换行*/

      .box {
        width: 100px;
        height: 130px;
        display: inline-block;
        border: 2px solid black;
        border-radius: 10px;
        margin-top: 30px;
        margin-left: -80px;
        transition: 0.1s;
      }
      .box:nth-child(1) {
        margin: 0;
        margin-left: 20px;
      }
      .box:nth-last-child(1) {
        margin-right: 20px;
      }
      .box:hover {
        width: 120px;
        height: 150px;
        margin-top: -20px;
      }
      .box img {
        width: 100%;
        height: 100%;
      }
    }
  }
}
</style>
