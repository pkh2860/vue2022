<template>
  <HeaderCont />
  <main id="main">
    <section class="refer__cont">
      <TitleCont name1="reference" name2="book" />
      <div class="container">
        <div class="refer__inner"></div>
      </div>
      <ContactCont />
    </section>
  </main>
  <FooterCont />
</template>
<script>
import HeaderCont from "@/components/HeaderCont.vue";
import FooterCont from "@/components/FooterCont.vue";
import TitleCont from "@/components/TitleCont.vue";
import ContactCont from "@/components/ContactCont.vue";
// import { ref } from "vue";

export default {
  components: {
    HeaderCont,
    TitleCont,
    FooterCont,
    ContactCont,
  },

  // setup() {
  //   const ports = ref([]);

  //   const Reference = () => {
  //     var requestOptions = {
  //       method: "GET",
  //       redirect: "follow",
  //     };

  //     fetch(
  //       "https://webstoryboy.github.io/react2022/src/assets/json/refer.json",
  //       requestOptions
  //     )
  //       .then((response) => response.text())
  //       .then((data) => console.log(type))
  //       .catch((error) => console.log("error", error));
  //   };

  //   setTimeout(() => {
  //     Reference();
  //   }, 2000);

  //   return {
  //     ports,
  //     Reference,
  //   };
  // },
};
</script>
<style lang="scss" scoped></style>
