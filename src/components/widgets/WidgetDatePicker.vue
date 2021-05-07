<template>
  <vue-interactjs
    :widget=widget
    :minw="100"
    :minh="30"
  >
    <div class="outer">
      <span :style="{color: widget.c, textAlign: widget.a}">{{ widget.t }}</span>
      <div class="inner clearfix"
        :style="{backgroundColor: widget.bc, textAlign: widget.a}"
      >
        <i class="material-icons float-right">date_range</i>

        <span class="left" style="{marginLeft: '50px'}">&nbsp;</span>
      </div>
    </div>
  </vue-interactjs>
</template>

<script>

  import VueInteractjs from '../../helpers/vue-interactjs'

  export default {
    props: [ 'widget' ],

    components: {
      'vue-interactjs': VueInteractjs
    }
  }

</script>

<style lang=scss scoped>
.outer{

    font-size: 18px;

    .inner {
      padding: 0;
      height: 30px;
      border:solid 3px rgba(15, 13, 13, 0.89);

      i {
        position: relative;
        top: -2px;
        margin-top: 2px;
      }

      span {
        position: relative;
        width: 22px;
        display: inline-block;
        height: 100%;
        margin-left: 10px;
      }
    }
  }

</style>
