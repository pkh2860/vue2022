<template>
  <HeaderCont />
  <main id="main">
    <section className="maincont">
      <div className="maininner">
        <div v-for="title in titles" v-bind:key="title.text">
          {{ title.text }}
        </div>
      </div>
    </section>
  </main>
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

  data: function () {
    return {
      titles: [
        { text: "we provide" },
        { text: "visual coding" },
        { text: "solution" },
        { text: "for you webs" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.maincont {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: var(--dark_bg);

  .maininner {
    font-size: 10vw;
    line-height: 0.85;
    font-family: var(--main_font);
    color: var(--white);
    text-transform: uppercase;
  }
}
</style>
