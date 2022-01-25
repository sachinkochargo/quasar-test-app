<template>
  <div class="q-pa-md q-gutter-sm">
    <h6 class="mb-2">GoButtonComponent</h6>
    <GoButton label="Save" elemType="gtp-detail" :dis="disabled" @onClickHandler="onClickHandler"/>
    <GoButton label="Submit" elemType="device-type" />
    <GoDropdownButton :filters="[dropDownButtonData]" label="Save Filter" />
    <GoAuthButton username="sachin" menuLinks="AUTH_MENU_ITEMS" />
    <!-- <QGrid /> -->
  </div>
  <div class="q-pa-md q-gutter-sm">
    <h6 class="mb-2">Go Cards</h6>
  </div>
  <div class="q-pa-md row items-start q-gutter-md">
    <GoCard
      title="This is a GO Card"
      cardType="gtp-detail"
      style="line-height: 0.5em"
    >
      <!-- <template> -->
      <div>
        <p>The body will come here !</p>
        <p>You can write a complete parahgraph</p>
        <p>Hi I am another parahgraph</p>
      </div>

      <!-- </template> -->
    </GoCard>
    <GoCardReview
      title="This is a GO Card"
      cardType="device-type"
      subtitle="this is a subtitle"
      description="this is a small desscrition"
      @onClickcHandler="onClickHandler"
      buttonTitle="Click Here"
    >
      <div>
        <p>The body will come here !</p>
        <h4>dakjhdkashdjkas</h4>
        <p>You can write a complete parahgraph</p>
        <p>Hi I am another parahgraph</p>
      </div>
    </GoCardReview>
  </div>
  <div style="padding: 20px">
    <h4>Go Table Cards</h4>
    <GoTableCard
      :tableStatsData="tableStatsData"
      title="OutBound"
      cardType="gtp-detail"
      style="line-height: 0.5em"
    >
      <div>
        <GoTable 
          :rows="rows"
          :columns="columns"
        />
      </div>
    </GoTableCard>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import {
  GoButton,
  GoCard,
  GoCardReview,
  GoTableCard,
  GoDropdownButton,
  GoAuthButton,
  GoTable
} from "go-component-library";
import {
  tableStatsData,
  dropDownButtonData,
  AUTH_MENU_ITEMS,
  TABLE_COLS,
  TABLE_ROW
} from "./../constants";
// import {QGrid} from 'quasar-ui-qgrid';
export default defineComponent({
  name: "PageIndex",
  components: {
    GoButton,
    GoCard,
    GoCardReview,
    GoTableCard,
    GoDropdownButton,
    GoAuthButton,
    GoTable
    // QGrid
  },
  methods: {
    onClickHandler: function () {
      alert("Action Called");
    },
  },
  data() {
    return {
      tableStatsData,
      dropDownButtonData,
      menuLinks : AUTH_MENU_ITEMS,
    };
  },
  setup(){
    return {
      columns : TABLE_COLS,
      rows : TABLE_ROW,
      disabled : false

    }
  }
  // computed : function(){
  //   return {
  //     tableStatsData : tableStatsData
  //   }
  // }
});
</script>
