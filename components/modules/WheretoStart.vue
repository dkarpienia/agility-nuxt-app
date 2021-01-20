<template>
  <div>
    <div class='col1'>
      <div class='image-col'>
        <img class='image' :src="item.fields.image.url" />    
      </div>
      <div class='bullet-list-col'>
        <h1>{{item.fields.title}}</h1>
        <div v-html="item.fields.bulletList" />
      </div>
    </div>
    <div class='col2'>
        <div v-html="item.fields.tipsTricks" />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    contentID: Number,
    item: Object,
    page: Object,
    pageInSitemap: Object,
    dynamicPageItem: Object
  }
};
</script>

<style scoped>

  .bullet-list-col {
    width: 45%;
    display: inline-block  
  }

  .col1 {
    width: 45%;
    display: inline-block
  }
  .col2 {
    width: 45%;
    display: inline-block
  }
  .image{
    height: 50px;
  }
  .image-col {
    width: 45%;
    display: inline-block 
  }


</style>