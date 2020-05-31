<template>
  <div>
    <button @click="isOpen = !isOpen">Control</button>
    <transition name="fade">
      <p v-if="isOpen">
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Maiores, ea.
        Adipisci dignissimos repellat eaque dolor provident incidunt, cumque
        aperiam quod repudiandae, tempora ea nobis laboriosam quis totam
        quibusdam in enim!
      </p>
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
  transition: background-color 300ms;
}
p {
  width: 300px;
  height: 300px;
  padding: 20px;
  margin: 0 auto;
}
.fade-enter {
  opacity: 0;
}
.fade-enter-active,
.fade-leave-active {
  transition: all 2s;
}
.fade-leave-to {
  opacity: 0;
}
</style>
