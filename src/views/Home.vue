<template>
  <div>
    <button @click="isOpen = !isOpen">Control</button>
    <div class="container" v-if="isOpen">
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Maiores, ea.
        Adipisci dignissimos repellat eaque dolor provident incidunt, cumque
        aperiam quod repudiandae, tempora ea nobis laboriosam quis totam
        quibusdam in enim!
      </p>
    </div>
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
  background-color: white;
  border: 2px solid #005fcc;
  padding: 5px;
  border-radius: 5px;
  transition: background-color 300ms;
  &:hover {
    background-color: #005fcc;
    color: #fff;
  }
}
.container {
  width: 300px;
  height: 300px;
  padding: 20px;
  margin: 0 auto;
}
</style>
