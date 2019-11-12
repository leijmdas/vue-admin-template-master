<template>
  <div class="dashboard-container">
    <div class="dashboard-text">name: {{ name }}</div>

    <el-carousel height="100%" width='100%' arrow="always" indicator-position="none"  >

          <div class="mask" v-show="true">
            <img name='img' src="../../assets/images/wallpaper.png" style="
                              width: 100%;
                              height: auto;"
                 alt=""  >
          </div>
    </el-carousel>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  name: 'Dashboard',
  computed: {
    ...mapGetters([
      'name'
    ])
  }
}
</script>

<style lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
  }
}
</style>
