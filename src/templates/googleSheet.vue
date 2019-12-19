<template>
   <Layout>
       <h3>Test Route</h3>
       <div>{{$page.googleSheet.Name}}</div>
       <h3>{{$page.googleSheet.Date}}</h3>

   </Layout>
</template>
<page-query>
query Post ($path: String!) {
    googleSheet(path: $path){
        Name
        Date
    }
}
</page-query>
<script>
export default {
    
}
</script>