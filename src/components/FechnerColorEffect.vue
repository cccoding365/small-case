<template>
  <h3>费希纳颜色效应</h3>
  <div class="box">
    <div class="circle">

      <div class="semicircle1"></div>
      <div class="line1 line-group1 line-group"></div>
      <div class="line2 line-group1 line-group"></div>
      <div class="line3 line-group1 line-group"></div>

      <div class="semicircle2"></div>
      <div class="line4 line-group2 line-group"></div>
      <div class="line5 line-group2 line-group"></div>
      <div class="line6 line-group2 line-group"></div>

      <div class="semicircle3"></div>
      <div class="line7 line-group3 line-group"></div>
      <div class="line8 line-group3 line-group"></div>
      <div class="line9 line-group3 line-group"></div>

      <div class="semicircle4"></div>
      <div class="line10 line-group4 line-group"></div>
      <div class="line11 line-group4 line-group"></div>
      <div class="line12 line-group4 line-group"></div>

      <div class="semicircle"></div>

    </div>
  </div>
</template>

<script setup></script>

<style lang="less" scoped>
* {
  margin: 0;
  padding: 0;
}

/*自定义动画类----顺时针旋转（使用这个动画的时候才设置动画执行时间）*/
@-webkit-keyframes changeright {

  0% {
    -webkit-transform: rotate(0deg);
  }

  50% {
    -webkit-transform: rotate(180deg);
  }

  100% {
    -webkit-transform: rotate(360deg);
  }
}

/*自定义动画类----逆时针旋转（使用这个动画的时候才设置动画执行时间）*/
@-webkit-keyframes changeleft {

  0% {
    -webkit-transform: rotate(0deg);
  }

  50% {
    -webkit-transform: rotate(-180deg);
  }

  100% {
    -webkit-transform: rotate(-360deg);
  }
}


.box {
  width: 300px;
  height: 300px;
  // border: 1px solid #000;

  .circle {
    width: 100%;
    height: 100%;
    border-radius: 50%;
    border: 1px solid rgba(0, 0, 0, .5);
    position: relative;
    -webkit-animation: changeleft .1s linear infinite;


    .line-group {
      position: absolute;
      left: 50%;
      top: 50%;
      box-sizing: border-box;
    }

    .semicircle1 {
      position: absolute;
      z-index: 7;
      left: 100px;
      top: 150px;
      width: 100px;
      height: 50px;
      background-color: #fff;
      border-bottom-left-radius: 50px;
      border-bottom-right-radius: 50px;
      transform-origin: top center;
      transform: rotate(225deg);
    }


    .semicircle2 {
      position: absolute;
      z-index: 5;
      left: 70px;
      top: 150px;
      width: 160px;
      height: 80px;
      background-color: #fff;
      border-bottom-left-radius: 80px;
      border-bottom-right-radius: 80px;
      transform-origin: top center;
      transform: rotate(45deg);
    }

    .semicircle3 {
      position: absolute;
      z-index: 3;
      right: 40px;
      top: 150px;
      width: 220px;
      height: 110px;
      background-color: #fff;
      border-bottom-left-radius: 110px;
      border-bottom-right-radius: 110px;
      transform-origin: top center;
      transform: rotate(-45deg);
    }

    .semicircle4 {
      position: absolute;
      z-index: 1;
      left: 10px;
      top: 150px;
      width: 280px;
      height: 140px;
      background-color: #fff;
      border-bottom-left-radius: 140px;
      border-bottom-right-radius: 140px;
      transform-origin: top center;
      transform: rotate(135deg);
    }

    .line-group1 {
      z-index: 6;
      border: 5px solid #000;
      transform: translate(-100%, -50%);
      border-right: transparent;
    }

    .line-group2 {
      z-index: 4;
      border: 5px solid #000;
      transform: translate(-100%, -50%);
      border-right: transparent;
    }

    .line-group3 {
      z-index: 2;
      border: 5px solid #000;
      transform: translate(0%, -50%);
      border-left: transparent;
    }

    .line-group4 {
      border: 5px solid #000;
      transform: translate(0%, -50%);
      border-left: transparent;
    }

    .line1 {
      width: 50px;
      height: 100px;
      border-top-left-radius: 50px;
      border-bottom-left-radius: 50px;
    }

    .line2 {
      width: 40px;
      height: 80px;
      border-top-left-radius: 40px;
      border-bottom-left-radius: 40px;
    }

    .line3 {
      width: 30px;
      height: 60px;
      border-top-left-radius: 30px;
      border-bottom-left-radius: 30px;
    }




    .line4 {
      width: 60px;
      height: 120px;
      border-top-left-radius: 60px;
      border-bottom-left-radius: 60px;
    }

    .line5 {
      width: 70px;
      height: 140px;
      border-top-left-radius: 70px;
      border-bottom-left-radius: 70px;
    }

    .line6 {
      width: 80px;
      height: 160px;
      border-top-left-radius: 80px;
      border-bottom-left-radius: 80px;
    }





    .line7 {
      width: 90px;
      height: 180px;
      border-top-right-radius: 90px;
      border-bottom-right-radius: 90px;
    }

    .line8 {
      width: 100px;
      height: 200px;
      border-top-right-radius: 100px;
      border-bottom-right-radius: 100px;
    }

    .line9 {
      width: 110px;
      height: 220px;
      border-top-right-radius: 110px;
      border-bottom-right-radius: 110px;
    }



    .line10 {
      width: 120px;
      height: 240px;
      border-top-right-radius: 120px;
      border-bottom-right-radius: 120px;
    }

    .line11 {
      width: 130px;
      height: 260px;
      border-top-right-radius: 130px;
      border-bottom-right-radius: 130px;
    }

    .line12 {
      width: 140px;
      height: 280px;
      border-top-right-radius: 140px;
      border-bottom-right-radius: 140px;
    }

    .semicircle {
      z-index: 999;
      position: absolute;
      bottom: 0;
      width: 300px;
      height: 150px;
      background-color: #000;
      border-bottom-left-radius: 150px;
      border-bottom-right-radius: 150px;
    }
  }
}
</style>