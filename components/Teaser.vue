<template>
  <div class="md:h-full bg-gradient-to-r from-indigo-500 via-purple-500 to-pink-500" v-editable="blok">
    <div class="teaser__inner">
      <h1>FlowerApps</h1>
      <h2>Create your flows with FlowerApps to help automate your business.</h2>
      <nuxt-link class="teaser__link" to="/documentation">Show me Samples</nuxt-link>
      <a
        class="teaser__link teaser__link--dark"
        href="https://github.com/flower-apps"
        target="_blank"
        rel="nofollow noopener"
        >Github</a
      >
    </div>
  </div>
</template>
  
  <script>
export default {
  props: ["blok"],
  computed: {
    teaser_styles: function () {
      return {
        backgroundImage: `url('${
          ""
        }')`,
      };
    },
  },
};
</script>
  
  <style lang="scss">
.teaser {
  background-size: cover;
  background-position: bottom;
  text-align: left;
  padding-top: 60px;
  background-repeat: no-repeat;
  background: rgb(237, 233, 255);
  color: rgb(10, 10, 10);

  // h1 {
  //   margin: 0;
  //   font-size: 3.5em;
  // }

  // h1,
  // h2 {
  //   font-weight: 300;
  // }
}

.teaser__inner {
  max-width: 1000px;
  padding: 20px 20px;
  margin: 0 auto;

  @media screen and (min-width: 840px) {
    padding-right: 250px;
  }
}

.teaser__link {
  position: relative;
  z-index: 1;
  display: inline-block;
  vertical-align: middle;
  padding: 10px 20px;
  outline: 0;
  font-family: inherit;
  font-weight: 500;
  line-height: 1.2222222;
  text-align: center;
  text-decoration: none;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  background: rgb(194, 53, 130);
  color: #fff;
  transform: translateY(0px);
  transition: transform 200ms ease;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  &:hover,
  &:focus {
    text-decoration: none;
    color: #fff;
    background-color: lighten(rgb(194, 53, 130), 5);
    transform: translateY(-1px);
    border-bottom: 0px;
  }
  & + .teaser__link {
    margin-left: 10px;
  }
}

.teaser__link--dark {
  background-color: #24292e;
  &:hover,
  &:focus {
    background-color: darken(#24292e, 5%);
  }
}
</style>