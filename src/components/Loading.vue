<template>
  <div class="loader loader3"></div>
</template>
<script>
export default {
  name: "VueLoading",

};
</script>
<style scoped>
.loader{
  width: 25px;
  height: 25px;
  display:flex;
  justify-content:center;
  align-items:center;
}
@keyframes load3{
  50%{
    transform:rotatez(180deg) scale(1.5);
    border-style:dotted;
  }
  100%{
    transform:rotatez(360deg) scale(0.9);
  }
}
.loader3::before{
  content:"";
  color:white;
  height:8px;
  width:8px;
  background:transparent;
  border-radius:50%;
  border:4px solid blue;
  border-color:#1565C0 #26C6DA;
  animation:load3 2s infinite;
}
</style>