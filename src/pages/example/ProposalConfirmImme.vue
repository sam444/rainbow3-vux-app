<template>
  <page>
       <top :title="$t('business.proposalConfirmImme')" :showBack="true"/>
       <r-body>
       <proposal-confirm-imme />
       </r-body>
       <bottom :index="2"/>
  </page>
</template>

<script>
import {Page,Card,RTable,RBody} from 'rainbow-mobile-core';
import Bottom from '../../components/Bottom';
import Top from '../../components/Top';
import ProposalConfirmImme from '../project/components/ProposalConfirmImme';

export default {
  components: {
    Bottom,
    Top,
    Page,
    Card,
    RTable,
    ProposalConfirmImme,
    RBody
  },
 
};
</script>

<style lang="less">

</style>

