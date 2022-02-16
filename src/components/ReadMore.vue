<script setup>
import {onMounted,ref,useAttrs} from 'vue';
import * as v from 'vue';
let props = defineProps({
  textTitle: {
    type: String,
    required: true
  },
  textCard: {
    required: true,
    type: String
  },
  textSeperate: {
    default: "...",
    type: String
  },
  lengthText: {
    type: Number,
    required: true
  }
})
var text = ref(props.textCard);

let isAbbreviation = true;

function changeString() {
  if (!isAbbreviation) {
    text.value = props.textCard;
  } else {
    let abbreviation = props.textCard.slice(0, props.lengthText).trim();
    abbreviation += props.textSeperate;
    text.value = abbreviation;
  }
  isAbbreviation = !isAbbreviation;
}

// changeString();

</script>

<template>
  <div class="row">
    <div class="col-3"></div>
    <div class="col-6">
      <div class="card">
        <div class="card-body">
          <h5 class="card-title">{{ textTitle }}</h5>
          <p class="card-text ">{{ text }}</p>
          <a href="#" @click.prevent="changeString" class="btn btn-primary">Read more</a>
        </div>
      </div>
    </div>
    <div class="col-3"></div>
  </div>
</template>

<style lang="scss">
.card {
  .card-text {
    text-align: justify;
  }
}


</style>
