<template>
  <div class="about">
    <h1>{{ testData }}</h1>
  </div>
</template>
<script>
import axios from 'axios'

export default {
  components: [],
  data() {
    return {
      testData: "",
    };
  },
  methods: {
    get() {
      axios.get('/api/connectTest')
        .then((response)=>{
          this.testData = response.data;
      });
    },
  },
  mounted() {
    this.get();
  },
};
</script>
