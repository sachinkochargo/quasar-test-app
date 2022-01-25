<template>
  <div class="q-pa-md row items-start q-gutter-md">
    <GoCard title="This is a GO Card" cardType="gtp-detail">
      <!-- <template> -->
      <div>
        <p>The body will come here !</p>
        <h4>dakjhdkashdjkas</h4>
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

      <!-- <template> -->
      <div>
        <p>The body will come here !</p>
        <h4>dakjhdkashdjkas</h4>
        <p>You can write a complete parahgraph</p>
        <p>Hi I am another parahgraph</p>
      </div>

      <!-- </template> -->
    </GoCardReview>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import { GoCard, GoCardReview } from "go-component-library";
export default defineComponent({
  name: "PageIndex",
  components: {
    GoCard,
    GoCardReview
  },
  methods : {
      onClickHandler : function(){
          alert('Action Called');
      }
  }
});
</script>
