<template>
  <div>
    <button type="button" @click="show = !show">点击我</button>
    <Clicaptcha
        v-if="show" :callback="callback" :src="src"/>
  </div>
</template>

<script>
import Clicaptcha from "@/components/Clicaptcha.vue";

export default {
  components: {
    Clicaptcha
  },
  data() {
    return {
      src: "http://127.0.0.1:8000/clicaptcha.php",
      show: false
    }
  },
  methods: {
    callback() {
      alert("yes");
    },
    captcha() {
      // Clicaptcha({
      //   src: "http://localhost/clicaptcha-server/clicaptcha.php",
      //   callback: () => {
      //     alert("yes");
      //   }
      // });
    }
  }
};
</script>
