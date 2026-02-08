<template>
<div class="page-wrapper">
  <div class="page" :id="$route.params.resumeid">
    <div class="page-inner">
      <component :is="$route.params.resumeid"></component>
    </div>
  </div>
</div>
</template>

<script>
import Vue from 'vue';
import '../resumes/resumes';
export default Vue.component('resume', {
    name: 'app'
});
</script>

<style scoped>
.page-inner{
  height: 100%;
  width: 100%;
}
.page-wrapper {
  overflow-x: hidden;
  background: #CCCCCC;
  margin: 0;
  padding: 0;
  -webkit-print-color-adjust: exact;
  box-sizing: border-box;
}

.resume {
  height: 100%;
  width: 100%;
}

.page {
  background: white;
  position: relative;
  width: 21cm;
  min-height: 29.68cm;
  display: block;
  page-break-after: auto;
  overflow: hidden;
  margin: 0 auto;
}

/* Tablet */
@media screen and (max-width: 900px) {
  .page {
    width: 100%;
    min-height: auto;
    height: auto;
    overflow: visible;
  }
}

/* Mobile */
@media screen and (max-width: 480px) {
  .page {
    width: 100%;
    min-height: auto;
    height: auto;
    overflow: visible;
  }
}

/* Print */
@media print {
  .page {
    width: 21cm;
    height: 29.68cm;
    overflow: hidden;
  }
}
</style>
