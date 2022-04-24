<template>
  <div class="item">
    <a :href="item.href" target="__blank">
      <i :class="item.icon" class="zoomIn"></i>
    </a>
    <span class="title"> {{ item.title }}</span>
  </div>
</template>

<script>
export default {
  name: "Item",
  created() {},
  data() {
    return {};
  },
  props: ["item"],
  methods: {},
};
</script>

<style lang="scss" scoped>
.item {
  display: flex;
  width: auto;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
  margin: 20px 50px;
  border-radius: 10px;
  padding: 20px 30px;
  background-color: rgba(255, 255, 255, 0.4);
  box-shadow: 0 10px 10px 10px rgba(0, 0, 0, 0.2);
}
.item img {
  width: 10rem;
  height: 10rem;

  border-radius: 80px;
}
.item .title {
  font-weight: 900;
  font-size: 1.8rem;
}
.item a {
  text-decoration: none;
  cursor: pointer;
  font-size: 7rem;
  color: #14c8fe;
  transition: all 0.5s ease;
}
.item a:hover {
  color: #005481;
}
.zoomIn {
  -webkit-animation-name: zoomIn;
  animation-name: zoomIn;
  -webkit-animation-duration: 3s;
  animation-duration: 3s;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
}
@-webkit-keyframes zoomIn {
  0% {
    opacity: 0;
    -webkit-transform: scale3d(0.3, 0.3, 0.3);
    transform: scale3d(0.3, 0.3, 0.3);
  }
  50% {
    opacity: 1;
  }
}
@keyframes zoomIn {
  0% {
    opacity: 0;
    -webkit-transform: scale3d(0.3, 0.3, 0.3);
    transform: scale3d(0.3, 0.3, 0.3);
  }
  50% {
    opacity: 1;
  }
}
</style>
