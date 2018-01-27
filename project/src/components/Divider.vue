<template>
<div class="divider"></div>
</template>

<script>
export default {
  name: 'divider',

  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.divider { 
    height: 8px;

    background: {
    image: url(../assets/img/dash.png);
    size: 30px 16px;
    }
}
</style>