<template>
  <div style="background-color: white; width: 500px; height: 500px">
    <div id="arcaptcha"></div>
  </div>
</template>

<script>
let script;
export default {
  created() {
    script = document.createElement("script");
    script.src = "https://widget.arcaptcha.ir/1/api.js?domain=localhost";
    document.body.appendChild(script);
  },

  mounted() {
    script.onload = () => {
      this.renderCaptcha();
    };
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
