<template>
  <vue-interactjs
    :widget=widget
    :minw="100"
    :minh="30"
  >
    <div class="outer-body">
    <span :style="{color: widget.c, textAlign: widget.a}">{{ widget.t }}</span>
    <div class="outer">
      <div class="inner" :style="{backgroundColor: widget.bc, textAlign: widget.a}">
        <div class="hr" :style="{borderTopColor: widget.c}">
          <table>
            <tr>
              <th>Data</th>
              <th>Data</th>
              <th>Data</th>
              <th>Data</th>
              <th>Data</th>
            </tr>
            <tr v-for="(item, index) in widget.d" :key="index">
                <td>{{ item.n }}</td>
                <td>{{ item.p }}</td>
                <td>{{ item.i }}</td>
                <td>{{ item.e }}</td>
                <td>{{ item.t }}</td>
            </tr>
          </table>
        </div>
      </div>
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
.outer-body{
  font-size: 18px;

  .outer {
    display: table;
    width: 100%;
    height: 100%;

    .inner {
      height: 10px;
      display: table-cell;
      vertical-align: middle;
      font-size: 1.4rem;

      table {
        border-top: 3px solid black;

        th {
            border: 3px solid black;
            padding: 0.5rem;
          }

        td {
            border: 3px solid black;
            padding: 20px;
        }

      }
    }
  }
  }

</style>
