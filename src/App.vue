<template>
  <div @click="open">Button</div>

  <widget-container-modal />
</template>

<script>
import { container, openModal } from "jenesius-vue-modal";
import ModalContent from "./components/ModalContent.vue";

export default {
  components: { WidgetContainerModal: container },
  methods: {
    open() {
      openModal(ModalContent);
    },
  },
  created() {
    const script = document.createElement("script");
    script.src = "https://widget.arcaptcha.ir/1/api.js?domain=localhost";
    document.body.appendChild(script);
  },
};
</script>
