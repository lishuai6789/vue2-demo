<template>
  <el-date-picker range-separator="至" value-format="timestamp" start-placeholder="开始日期" end-placeholder="结束日期" required clearable
    :default-time="['00:00:00', '23:59:59']" type="daterange" v-model="date" @change="handleChange"></el-date-picker>
</template>
<script>
export default {
  name: "WmsDatePicker",
  data() {
    return {
      date: '',
    };
  },
  methods: {
    handleChange(date) {
      if (date) {
        this.$emit('input', [date[0] / 1000, date[1] / 1000]);
      } else {
        this.$emit('input', '');
      }
    },
  },
};
</script>
