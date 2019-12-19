<template>
  <Layout>

    <!-- Learn how to use images here: https://gridsome.org/docs/images -->


    <h1>Hello, world!</h1>
    <div v-for="page in $page.allGoogleSheet.edges" :key="page.id">
      {{page.node.Name}}
      {{page.node.Age}}
    </div>


  </Layout>
</template>
<page-query>
  query {
    allGoogleSheet {
      edges {
        node {
        Name
        Age
        Id
    }
  }
}
  }
</page-query>

<script>
export default {
  metaInfo: {
    title: 'Hello, world!'
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
