<template>
  <div>
    <input type="text" v-model="code" />
    <!-- prettier-ignore -->
    <button @click="openCode">▶</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      code: ""
    };
  },
  methods: {
    openCode() {
      const openNewBackgroundTab = url => {
        const anchor = document.createElement("a");
        anchor.href = url;
        document.body.appendChild(anchor);
        const evt = document.createEvent("MouseEvents");
        // the tenth parameter of initMouseEvent sets ctrl key
        evt.initMouseEvent(
          "click",
          true,
          true,
          window,
          0,
          0,
          0,
          0,
          0,
          true,
          false,
          false,
          false,
          0,
          null
        );
        anchor.dispatchEvent(evt);
      };
      openNewBackgroundTab(`https://nhentai.net/g/${this.code}`);
    }
  }
};
</script>

<style></style>
