<template>
  <page>
       <top :title="$t('component.previewer')" :showBack="true"/>
       <r-body>
          <card>
            <previewer :title="$t('preview.totle')" :value="`${this.$t('common.currency')} 1024`" :data="list" />
          </card>
          <card>
            <previewer :title="$t('preview.totle')" :value="`${this.$t('common.currency')} 1024`"  :data="list" :buttons="buttons1"/>
          </card>
          <card>
            <previewer :title="$t('preview.totle')" :value="`${this.$t('common.currency')} 1024`"  :data="list" :buttons="buttons2" :param="param"/>
          </card>
       </r-body>
       <bottom :index="2"/>
  </page>
</template>

<script>
import {Page,Card,RBody} from 'rainbow-mobile-core';
import {Previewer} from 'rainbow-mobile-previewer';
import Bottom from '../../components/Bottom';
import Top from '../../components/Top';

export default {
  components: {
    Bottom,
    Top,
    Page,
    Previewer,
    Card,
    RBody
  },
  data(){
    return {
      param:{name:'Rainbow'}
    }
  },
  computed:{
    list(){
      return [{
        label: this.$t('preview.goods'),
        value: this.$t('preview.machine')
      }, {
        label: this.$t('preview.title'),
        value: this.$t('preview.title')
      }, {
        label: this.$t('preview.name'),
        value: this.$t('preview.longName')
      }]
    },
    buttons1(){
      return [{
        style: 'default',
        text: this.$t('preview.left')
      }, {
        style: 'primary',
        text: this.$t('preview.right'),
        link: '/'
      }]
    },
    buttons2(){
      return [{
        style: 'primary',
        text: this.$t('preview.click'),
        onButtonClick: (param) => {
          alert(`I Love ${param.name} Mobile`)
        }
    }]}
  }
};
</script>



