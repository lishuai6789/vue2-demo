<template>
  <div class="home">
    <p>Height: {{ height }}</p>
    <div>
      <WmsDatePicker v-model="date"></WmsDatePicker>
    </div>
    <el-divider></el-divider>
    <p>{{ date }}</p>
    <el-divider></el-divider>
    <el-table :max-height="tableMaxHeight" border></el-table>
  </div>
</template>
<script>
import WmsDatePicker from '@/components/WmsDatePicker.vue';

export default {
  name: 'HomeView',
  components: {
    WmsDatePicker
  },
  data() {
    return {
      date: ['', ''],
      tableMaxHeight: '',
    }
  },
  created() {
  },
  methods: {
    handleDatePickerChange(val) {
      console.log(val);
      this.date = val;
    },
    handleWindowChange(e) {
      if (e.matches) {
        this.height = 1920;
      }
    },
    handleSecondChange(e) {
      if (e.matches) {
        this.height = 1280;
      }
    }
  },
}
</script>
<style scoped>
.home {}

.container {
  width: 100%;
  height: 100px;
}
</style>