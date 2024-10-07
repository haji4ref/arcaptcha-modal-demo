<template>
  <div style="background-color: white; width: 500px; height: 500px">
    <div id="arcaptcha"></div>
  </div>
</template>

<script>
export default {
  mounted() {
    this.renderCaptcha();
  },
  methods: {
    renderCaptcha() {
      window.arcaptcha.render(document.getElementById("arcaptcha"), {
        site_key: "d6ggpvy684",
      });
    },
  },
};
</script>
