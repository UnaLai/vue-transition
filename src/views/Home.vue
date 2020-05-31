<template>
  <div>
    <button @click="isOpen = !isOpen">Control</button>
    <!-- <transition name="fade">
      <p v-if="isOpen">
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Maiores, ea.
        Adipisci dignissimos repellat eaque dolor provident incidunt, cumque
        aperiam quod repudiandae, tempora ea nobis laboriosam quis totam
        quibusdam in enim!
      </p>
    </transition> -->
    <transition name="fade" mode="out-in">
      <p v-if="isOpen">
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Maiores, ea.
        Adipisci dignissimos repellat eaque dolor provident incidunt.
      </p>
      <div v-else class="box"></div>
    </transition>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      isOpen: false
    };
  }
};
</script>
<style lang="scss" scoped>
button {
  background-color: #005fcc;
  color: #fff;
  border: 2px solid #005fcc;
  padding: 5px;
  border-radius: 5px;
  margin-bottom: 10px;
}
p {
  width: 300px;
  padding: 20px;
  margin: 0 auto;
}
.box {
  width: 300px;
  height: 100px;
  background-color: pink;
  margin: 0 auto;
}
.fade-enter {
  opacity: 0;
  transform: translateX(-10px);
}
.fade-enter-active,
.fade-leave-active {
  transition: all 1s;
}
.fade-leave-to {
  opacity: 0;
  transform: translateX(-10px);
}
</style>
