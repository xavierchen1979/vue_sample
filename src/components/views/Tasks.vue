<template>
  <section class="content">
    task page
  </section>
</template>
<script>
  import moment from 'moment'
  import {timeline} from '../../demo'

  export default {
    name: 'Tasks',
    computed: {
      today () {
        return moment().format('MMM Do YY')
      },
      timeline () {
        return timeline
      }
    }
  }
</script>

<style>
  
</style>
