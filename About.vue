<template>
  <div class="about">
    <h1>This is an about page</h1>
    <p>{{ now }}</p>
  </div>
</template>

<script>
export default {

  data() {
    return {
      now: new Date()
    }
  },
  methods: {
    updateDate() {
      this.now = new Date();
    }
  },
  mounted() {
    setInterval(() => {
      this.updateDate();
    }, 1000);
  }

}
</script>

<style scoped>
p{
  margin: 20px 0;
}
</style>
