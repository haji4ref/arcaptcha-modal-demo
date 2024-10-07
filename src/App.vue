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
  created() {},
};
</script>
