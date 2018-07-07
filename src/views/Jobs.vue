<template>
  <div class="wrapper">
    <div class="jobs">
      <h1>Jobs</h1>
      <label for="jobs"></label>
      <input
      id='jobs'
      name='jobs'
      v-model='jobsValue'
      @input='handleInput'
      />
    </div>
  </div>
</template>

<script>
export default {
  name: 'Jobs',
  data() {
    return {
      jobsValue: '',
    };
  },
  methods: {
    handleInput() {
      console.log(this.jobsValue);
    },
  },
};
</script>

<style lang='scss' scoped>
.wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0;
  padding: 30px;
  width: 100%;
}
</style>
