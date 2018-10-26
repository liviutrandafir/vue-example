<template>
  <b-container class="bv-example-row">
    <b-row>
      <b-col col sm="12" md="12" lg="2">
        <PageSidebar />
      </b-col>
      <b-col col sm="12" md="12" lg="10">
        <PageCover />
        <PageContent />
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import PageSidebar from '@/components/PageSidebar.vue';
import PageCover from '@/components/PageCover.vue';
import PageContent from '@/components/PageContent.vue';

export default {
  name: 'HomePage',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components: {
    PageSidebar,
    PageCover,
    PageContent,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
