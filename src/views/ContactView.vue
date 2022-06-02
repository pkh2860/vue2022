<template>
  <HeaderCont />
  <section className="contact__cont">
    <div className="container">
      <div className="contact__inner">
        <div className="text">
          <div>You are</div>
          <div>already</div>
          <div>doing well.</div>
        </div>
        <p className="desc">
          같은 목표를 위해 달려갈 웹 퍼블리셔 & 프론트 앤드 개발자를 모집합니다.
          관심 있는 분들은 카카오톡 또는 카페에 문의해주세요.
        </p>
      </div>
    </div>
  </section>
  <FooterCont />
</template>
<script>
import HeaderCont from "@/components/HeaderCont.vue";
import FooterCont from "@/components/FooterCont.vue";

export default {
  components: {
    HeaderCont,
    FooterCont,
  },
};
</script>

<style lang="scss" scoped>
.contact__cont {
  background-color: var(--dark_bg);
  height: 100vh;
}
.contact__inner {
  color: var(--white);
  align-content: center;
  justify-content: center;
  display: flex;
  flex-wrap: wrap;
  height: 100vh;

  .text {
    font-size: 9vw;
    line-height: 0.85;
    font-family: var(--main_font);
    text-transform: uppercase;
    width: 100%;

    div:nth-child(2) {
      text-align: center;
      padding-right: 13vw;
    }

    div:nth-child(3) {
      text-align: right;
    }
  }
  .desc {
    margin-left: 70%;
    text-align: left;
    font-size: 1rem;
    font-family: var(--kor_font);
    line-height: 1.5;
    padding-top: 2rem;
  }
}

@media (max-width: 1200px) {
  .contact__inner {
    .text {
      div {
        text-align: center;
      }
      div:nth-child(2) {
        text-align: center;
        padding-right: 0;
      }
      div:nth-child(3) {
        text-align: center;
      }
    }
    .desc {
      margin-left: 0;
      width: 40vw;
      text-align: center;
      word-break: keep-all;
    }
  }
}

@media (max-width: 600px) {
  .contact__inner {
    .text {
      font-size: 60px;
    }
    .desc {
      width: 90vw;
    }
  }
}
</style>
