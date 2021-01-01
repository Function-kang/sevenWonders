<template>
  <div class="start">
    <div class="left">
      <user></user>
      <user class="bottom"></user>
    </div>
    <div class="right">
      <div class="progress">
        <!-- 本局可发展科技 -->
        <img src="../assets/images/ycy.jpg" alt="" />
        <img src="../assets/images/ycy.jpg" alt="" />
        <img src="../assets/images/ycy.jpg" alt="" />
        <img src="../assets/images/ycy.jpg" alt="" />
        <img src="../assets/images/ycy.jpg" alt="" />
      </div>
      <ul class="attack">
        <!-- 攻击进度条 -->
        <li class="in"></li>
        <li class="in"></li>
        <li class="in"></li>
        <li class="in"></li>
        <li class="in"></li>
        <li class="in"></li>
        <li class="in"></li>
        <li class="in"></li>
        <li class="in"></li>
        <li class="in"></li>
        <li class="in"></li>
        <li class="in"></li>
        <li class="in"></li>
        <li class="in"></li>
        <li class="in"></li>
        <li class="in"></li>
        <li class="in"></li>
        <li class="in"></li>
        <li class="in"></li>
      </ul>
      <div class="effect">
        <!-- 军事效果标记 -->
      </div>
      <ul v-for="(value, index) in cardData.data" :key="index" class="list">
        <li
          class="card"
          v-for="(val, ind) in value"
          :key="ind"
          @click="cardClick(val, index, ind)"
        >
          {{ val.value }}
        </li>
      </ul>
    </div>
    <relicSelect
      class="relicSelect"
      v-show="relicSelectShow"
      @clone="relicSelectClone"
    ></relicSelect>
  </div>
</template>

<script>
import era from "../store/gameData";
import user from "./user.vue";
import relicSelect from "./relicSelect.vue";
export default {
  name: "start",
  props: {
    msg: String,
  },
  data() {
    return {
      arr: [],
      cardData: {},
      relicSelectShow: true,
    };
  },
  mounted() {
    // this.arr = era.one;
    this.cardData = era.two;
  },
  methods: {
    cardClick(obj, index, ind) {
      /*

        obj：当前点击卡牌的数据
        index：行 ul 的下标
        ind：列 li 卡牌在当前行的下标

      */
      // console.log(obj, index, ind)

      const { value, deep, show } = obj;
      // console.log(value, deep, show)

      let card = document.getElementsByClassName("card");
      if (deep) {
        let temp = 0;
        for (let i = 0; i < this.cardData.data.length - (this.cardData.data.length - index); i++) {
          temp = temp + this.cardData.data[i].length;
        }
        temp += ind; // temp 是所有卡牌自左向右自上而下的下标值，从 0 开始数
        // console.log(temp)

        // console.log("取下卡牌")




        // 取下卡牌
        if(index !== this.cardData.data.length-1){
          if(this.cardData.id == "one"){
            // console.log("one")
            if(this.cardData.data[index+1][ind].show == false && this.cardData.data[index+1][ind+1].show == false){
              this.cardData.data[index][ind].show = false;
              card[temp].style.visibility = "hidden";
            }
          }else if(this.cardData.id == "two"){
            console.log("two取下卡牌")
            // console.log(obj)
            console.log(this.cardData.data[index+1][ind].show)
            console.log(this.cardData.data[index+1][ind+1].show)
            console.log(this.cardData.data[index][ind].show)

            // if(ind == 0){

            // }else if(ind == )


            if((ind !== 0 || ind !== this.cardData.data[index].length-1)&&(this.cardData.data[index+1][ind].show == false && this.cardData.data[index+1][ind+1].show == false)){
              this.cardData.data[index][ind].show = false;
              card[temp].style.visibility = "hidden";
            }else if(ind == 0 || ind == this.cardData.data[index].length-1){
              
            }
          }
        }else{
          this.cardData.data[index][ind].show = false;
          card[temp].style.visibility = "hidden";
        }
      }

      if(this.cardData.id == "one"){
        // 通过循环修改卡片正反面
        for(let i = 0;i < this.cardData.data.length;i++){
          for(let j = 0;j < this.cardData.data[i].length;j++){
            if(this.cardData.data[i][j].deep == false && this.cardData.data[i][j].show == true){
              if(this.cardData.data[i+1][j].show == false && this.cardData.data[i+1][j+1].show == false){
                this.cardData.data[i][j].value = "正面" + (i + 1) + "-" + (j + 1);
                this.cardData.data[i][j].deep = true;
              }
            }
          }
        }
      }else if(this.cardData.id == "two"){
        for(let i = 0;i < this.cardData.data.length;i++){ // i 是循环行
          for(let j = 0;j < this.cardData.data[i].length;j++){ // j 是循环列
            if(this.cardData.data[i][j].deep == false && this.cardData.data[i][j].show == true){ // 当卡牌为反面，并且还在场上
              if(j == 0){
                if(this.cardData.data[i+1][j].show == false){
                  this.cardData.data[i][j].value = "正面" + (i + 1) + "-" + (j + 1);
                  this.cardData.data[i][j].deep = true;
                }
              }else if(j == this.cardData.data[i].length-1){
                if(this.cardData.data[i+1][this.cardData.data[i+1].length-1].show == false){
                  this.cardData.data[i][j].value = "正面" + (i + 1) + "-" + (j + 1);
                  this.cardData.data[i][j].deep = true;
                }
              }else{
                if(this.cardData.data[i+1][j].show == false && this.cardData.data[i+1][j-1].show == false){
                  this.cardData.data[i][j].value = "正面" + (i + 1) + "-" + (j + 1);
                  this.cardData.data[i][j].deep = true;
                }
              }
            }
          }
        }
      }
    },
    relicSelectClone(value) {
      this.relicSelectShow = value;
    },
  },
  components: {
    user,
    relicSelect,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.start {
  width: 100%;
  height: 100%;
  background: blue;
  display: flex;
  position: relative;

  .left {
    flex: 1;
    display: flex;
    flex-direction: column;
    background: pink;
    overflow: hidden;

    .bottom {
      border-top: 1px solid black;
    }
  }
  .right {
    flex: 1;
    .progress {
      width: 70%;
      height: 90px;
      background: red;
      margin: 0 auto;
      margin-top: 10px;
      display: flex;
      align-items: center;
      justify-content: space-around;
      border-radius: 0;
      border-top-right-radius: 15px;
      border-top-left-radius: 15px;

      img {
        width: auto;
        height: 80%;
        border-radius: 50%;
      }
    }
    .attack {
      width: 100%;
      height: 70px;
      background: rgb(206, 82, 206);
      display: flex;
      align-items: center;
      justify-content: space-around;
      margin: 0;

      .in {
        width: 30px;
        height: 90%;
        background: red;
        border-radius: 50%;
      }
    }
    .effect {
      width: 90%;
      height: 70px;
      background: red;
      margin: 0 auto;
      margin-bottom: 70px;
      border-bottom-left-radius: 15px;
      border-bottom-right-radius: 15px;
    }
    .list {
      text-align: center;
      margin-top: -50px;
      .card {
        width: 80px;
        height: 110px;
        border: 1px solid black;
        display: inline-block;
        background: yellow;
        margin-left: 10px;
      }
      .card:nth-child(1) {
        margin-left: 0;
      }
    }
  }
}
</style>
