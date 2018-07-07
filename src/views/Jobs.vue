<template>
  <div class="wrapper">
    <div class="jobs">
      <h1>Jobs</h1>
      <ul>
        <li v-for="job in jobs">
          {{ job.title }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'Jobs',
  data() {
    return {
      jobs: [],
    };
  },
  mounted() {
    axios.get('http://localhost:3000/api/v1/jobs')
      .then((response) => {
        this.jobs = response.data;
      })
      .catch((error) => {
        console.log(error);
      });
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
