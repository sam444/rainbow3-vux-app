<template>
  <page>
       <top :title="$t('component.form')" :showBack="true"/>
       <r-body>
       </r-body>
       
       <bottom :index="2"/>
  </page>
</template>

<script>
import {Page,RForm,RBody} from 'rainbow-mobile-core';
import Bottom from '../../components/Bottom';
import Top from '../../components/Top';

export default {
  components: {
    Bottom,
    Top,
    Page,
    RForm,
    RBody
  },
};
</script>

<style lang="less">

</style>

