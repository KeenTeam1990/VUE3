<template>
  <div class="app-container">
    <!-- <div class="top">
      <div class="tszl" @click="goPage('/external/connector')">
        <p class="dtitle">接入外部接口数量</p>
        <p class="total">{{partyApiNum}} 个 </p>
      </div>
      <div class="ljdl" @click="goPage('/api/api')">
        <p class="dtitle">平台发布接口数量</p>
        <p class="total">{{apiNum}} 个 </p>
      </div>
      <div class="ljfw" @click="goPage('/api/apiCount')">
        <p class="dtitle">平台接口累计访问量</p>
        <p class="total">{{apiRecordSums}} 次 </p>
      </div>
      <div class="jffw" @click="goPage('/api/apiCount')">
        <p class="dtitle">平台计费接口访问量</p>
        <p class="total">{{chargeApiRecdSums}} 次 </p>
      </div>
    </div> -->
    <div class="main">
      <div id="curfw"></div>
    </div>
  </div>
</template>

<script>

  export default {
    name: "dashboard",
    data(){
      return {
        apiRecordSums:'9315',
        chargeApiRecdSums:'8085',
        partyApiNum:'42',
        apiNum:'69',
        groupId:'',
      }
    },
    created() {

    },
    methods:{
      groupChange(){
      },
   
      goPage(route){
      },

    }
  }
</script>

<style scoped lang="scss">
  .top{
    width: 100%;
    display: flex;
    justify-content: space-between;
    .ljfw,.ljdl,.jffw,.tszl{
      width: 20.2%;
      height:  0.83rem ;
      padding: 0.125rem 0.2rem 0.125rem 0.2rem;

      border-radius: 0.2rem;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      color: #ffffff;
      p{
        margin: 0;
      }
      .dtitle{
        font-size:  0.16rem;
        font-weight: bold;
        white-space: nowrap;
      }
      .total{
        font-size: 0.21rem;
        text-align: right;
        margin-right: 0.24rem;
        font-weight: bold;
        white-space: wrap;
      }
      .count,.rise{
        font-size: 0.125rem;
      }
    }
    .ljfw:hover,.ljdl:hover,.jffw:hover,.tszl:hover{
      cursor: pointer;
    }
    .ljdl{
      box-shadow: 2px 6px 6px #c1ea90;
      background: -webkit-linear-gradient(left, #43d799 , #a4e261);
    }
    .ljfw{
      box-shadow: 2px 6px 6px #80c8f7;
      background: -webkit-linear-gradient(left, #40abf7 , #727cfc);
    }
    .jffw{
      box-shadow: 2px 6px 6px #f3c5cc;
      background: -webkit-linear-gradient(left, #ea687c , #ef9a60);
    }
    .tszl{
      box-shadow: 2px 6px 6px #e2bcfa;
      background: -webkit-linear-gradient(left, #5c72fd , #c87afd);
    }
  }
  .main{
    margin-top: 35px;
    box-shadow: 1px 6px 6px 6px #cccccc;
    padding: 20px;
 
  }
</style>
