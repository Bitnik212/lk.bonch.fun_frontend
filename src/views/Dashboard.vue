<template>
  <div>
    <base-header class="pb-8 pt-7 bg-gray">
       <b-row>
         <div class="h1 text-white m-3">Новости колледжа</div>
       </b-row>
     
      
    </base-header>
     
    <!--Charts-->
    <b-container fluid class="mt--8">
      <b-row>
        
        <News></News>
      </b-row>
    </b-container>

  </div>
</template>
<script>

import News from "@/components/News/News"

  export default {
    components: {
      
    },
    data() {
      return {
       
      };
    },
    methods: {
      
    },
    mounted() {
    }
  };
</script>
<style>
.el-table .cell{
  padding-left: 0px;
  padding-right: 0px;
}
</style>
