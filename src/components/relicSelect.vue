<template>
  <div class="relicSelect">
    <div class="box">
      <div class="header">
        <span class="title">选择本局遗迹</span>
        <span class="clone" @click="clone">×</span>
      </div>
      <div class="main">
        <div class="row">
          <div class="col-md-3 relicCard">
            <img src="../assets/images/hczz.jpg" alt="" />
          </div>
          <div class="col-md-3 relicCard">
            <img src="../assets/images/hczz.jpg" alt="" />
          </div>
          <div class="col-md-3 relicCard">
            <img src="../assets/images/hczz.jpg" alt="" />
          </div>
          <div class="col-md-3 relicCard">
            <img src="../assets/images/hczz.jpg" alt="" />
          </div>
        </div>
        <div class="row">
          <div class="col-md-3 relicCard">
            <img src="../assets/images/hczz.jpg" alt="" />
          </div>
          <div class="col-md-3 relicCard">
            <img src="../assets/images/hczz.jpg" alt="" />
          </div>
          <div class="col-md-3 relicCard">
            <img src="../assets/images/hczz.jpg" alt="" />
          </div>
          <div class="col-md-3 relicCard">
            <img src="../assets/images/hczz.jpg" alt="" />
          </div>
        </div>
        <div class="row">
          <div class="col-md-3 relicCard">
            <img src="../assets/images/hczz.jpg" alt="" />
          </div>
          <div class="col-md-3 relicCard">
            <img src="../assets/images/hczz.jpg" alt="" />
          </div>
          <div class="col-md-3 relicCard">
            <img src="../assets/images/hczz.jpg" alt="" />
          </div>
          <div class="col-md-3 relicCard">
            <img src="../assets/images/hczz.jpg" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  methods: {
    clone() {
      this.$emit("clone", false);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.relicSelect {
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: absolute;
  top: 0;
  left: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  .box {
    width: 85%;
    height: 80%;
    background: rgb(219, 219, 219);
    border-radius: 15px;
    display: flex;
    flex-direction: column;
    .header {
      width: 100%;
      height: 7%;
      background: rgb(65, 65, 65);
      border-top-left-radius: 15px;
      border-top-right-radius: 15px;
      color: white;
      display: flex;
      align-items: center;
      justify-content: space-between;
      .title {
        float: left;
        margin-left: 2%;
      }
      .clone {
        float: right;
        margin-right: 1%;
        font-size: 30px;
      }
    }
    .main {
      flex: 1;
      border-bottom-left-radius: 15px;
      border-bottom-right-radius: 15px;
      overflow: auto;
      .row {
        width: 100%;
        height: 30%;
        margin-top: 10px;
        .relicCard {
          height: 100%;
          img {
            width: 100%;
            height: 100%;
          }
        }
      }
    }
  }
}
</style>
