<template>
  <page>
       <top :title="$t('component.dialog')" :showBack="true"/>
       <r-body>
            <card :title="$t('component.basic')">
              <r-switch :title="$t('dialog.show')" :model="policy" value="show1" :onClick="onClick"></r-switch>
              <r-switch :title="$t('common.api')" :model="policy" value="show2" :onClick="clickSwitchApi"></r-switch>
              <alert  :model="policy" value="show1" :title="$t('row.title')" :onHide="onHide" :onShow="onShow" > {{ $t('divider.sogo') }}</alert>
            </card>
       </r-body>
       <bottom :index="2"/>
  </page>
</template>

<script>
import { Page, Card, RSwitch, Alert, AlertApi,RBody } from "rainbow-mobile-core";
import Bottom from "../../components/Bottom";
import Top from "../../components/Top";
import dialog from "../../assets/dialog.jpg";

export default {
  components: {
    Bottom,
    Top,
    Page,
    Card,
    RSwitch,
    Alert,
    RBody
  },
  data() {
    return {
      policy: {}
    };
  },
  methods: {
    onClick() {
      console.log("click");
    },
    clickSwitchApi(val) {
      const self = this;
      AlertApi.show({
        title: this.$t("row.title"),
        content: this.$t("divider.sogo"),
        onShow() {
          console.log("Module: I'm showing");
        },
        onHide() {
          self.policy.show2 = false;
          console.log("Module: I'm hiding now");
        }
      });
    },
    onHide() {
      console.log("Hide");
    },
    onShow() {
      console.log("show");
    }
  }
};
</script>



