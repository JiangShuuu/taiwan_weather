<template>
  <div class="main">
    <div class="main_container">
      <div class="box_1">
        <p class="current_summary">多雲轉陰</p>
        <p class="current_temper">12</p>
      </div>
      <div class="explain_2 d-none">
        <p>
          淡水區目前多雲轉陰，氣溫 12 度。預計今日溫度介於 11 到 15
          度之間，降雨機率約 10%。
        </p>
      </div>
      <div class="box_2">
        <div class="date">
          <p>星期三</p>
          <p class="date_min">今天</p>
        </div>
        <div class="min_temper">
          <p class="height_temper">15</p>
          <p class="low_temper">11</p>
        </div>
      </div>
      <div class="box_3">
        <div class="card">
          <p class="card_time">現在</p>
          <p class="card_percent">10%</p>
          <p class="card_icon">hi</p>
          <p class="card_temper">12</p>
        </div>
      </div>
      <div class="box_4">
        <div class="card">
          <div class="card_date">星期四</div>
          <div class="card_icon">Hi</div>
          <div class="card_temper">
            <p class="height_temper">16</p>
            <p class="low_temper">12</p>
          </div>
        </div>
      </div>
      <div class="explain_1">
        <p>
          淡水區目前多雲轉陰，氣溫 12 度。預計今日溫度介於 11 到 15
          度之間，降雨機率約 10%。
        </p>
      </div>
    </div>
    <div class="main_detail">
      <div class="card">
        <div class="card_title">日出</div>
        <div class="card_detail">上午 6:42</div>
      </div>
      <div class="card">
        <div class="card_title">日落</div>
        <div class="card_detail">下午 6:42</div>
      </div>
      <div class="card">
        <div class="card_title">降雨機率</div>
        <div class="card_detail">70%</div>
      </div>
      <div class="card">
        <div class="card_title">溫度</div>
        <div class="card_detail">80%</div>
      </div>
      <div class="card">
        <div class="card_title">風</div>
        <div class="card_detail">東北 6 公尺 / 秒</div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import "../assets/scss/All.scss";
.main {
  @include flexCenter;
  flex-direction: column;
  text-align: center;
  color: white;
  @include pad {
    flex-direction: row;
  }
  &_container {
    width: 80%;
    .box_1 {
      .current_summary {
        font-size: 10px;
      }
      .current_temper {
        font-size: 60px;
        font-weight: 200;
        font-family: "Work Sans";
      }
    }
    .box_2 {
      @include flexCenter;
      justify-content: space-between;
      width: 100%;
      padding: 0.25rem 0.75rem;
      border-bottom: 1px solid white;
      .date {
        display: flex;
        align-items: flex-end;

        &_min {
          margin-left: 0.25rem;
          font-size: 10px;
        }
      }
      .min_temper {
        display: flex;
        .low_temper {
          margin: 0 0.5rem 0 1rem;
          opacity: 0.55;
        }
      }
    }
    .box_3 {
      font-size: 10px;
      padding: 0.25rem 0.75rem;
      border-bottom: 1px solid white;
      .card {
        width: 10%;
      }
    }
    .box_4 {
      padding: 0.25rem 0.75rem;
      border-bottom: 1px solid white;
      .card {
        @include flexCenter;
        justify-content: space-between;
        &_temper {
          display: flex;
          .low_temper {
            margin: 0 0.45rem 0 1rem;
            opacity: 0.55;
          }
        }
      }
    }
    .explain_1 {
      padding: 0.25rem 0.75rem;
      text-align: start;
      border-bottom: 1px solid white;
      @include pad {
        display: none;
      }
    }
    .explain_2 {
      @include pad {
        display: block;
      }
      padding: 0.25rem 0.75rem;
      text-align: start;
      border-bottom: 1px solid white;
    }
  }
  &_detail {
    display: flex;
    justify-content: flex-start;
    flex-direction: column;
    width: 80%;
    border: 1px solid;
    padding: 0.25rem 0.75rem;
    .card {
      text-align: start;
      margin-bottom: 0.75rem;
      &_title {
        font-size: 10px;
      }
      &_detail {
        font-size: 24px;
      }
    }
  }
}
</style>
