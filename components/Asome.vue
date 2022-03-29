<!--
 * @Author: codesides
 * @Descripttion: 
 * @Date: 2022-03-15 15:41:51
 * @LastEditors: codesides
 * @LastEditTime: 2022-03-29 17:13:08
 * @FilePath: /nuxt3/components/Asome.vue
-->
<template>
  <div>
    <button @click="change">changesss</button>
    <iframe
      ref="iframe"
      src="http://10.80.102.112:8080/#?main_id=122278"
      frameborder="0"
      style="width: 1000px; height: 600px"
    ></iframe>
  </div>
</template>

<script lang='ts'>
import { defineComponent, reactive, toRefs } from "vue";

export default defineComponent({
  name: "Asome",
  props: {},
  components: {},
  setup() {
    const a = ref(0);
    return {
      a,
    };
  },
  methods: {
    change() {
      this.$refs.iframe.contentWindow.addMark("哈哈哈");
    },
    /**
     * @description:
     * @param {*} a
     * @param {*} b
     * @return {*}
     */
    test(a, b) {
      return a + b;
    },
  },
});
</script>

<style scoped>
.a {
  font-size: 14px;
}
</style>