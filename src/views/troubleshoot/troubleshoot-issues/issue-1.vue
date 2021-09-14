<template>
  <div id="issue1">
    
    <Introduction> </Introduction>
    <Causes></Causes>
    <Explanations></Explanations>

  </div>
</template>



<style>


</style>

<script>
// @ is an alias to /src
import Introduction from '@/components/troubleshoot/troubleshoot-issues/Introduction.vue'
import Causes from '@/components/troubleshoot/troubleshoot-issues/Causes.vue'
import Explanations from '@/components/troubleshoot/troubleshoot-issues/Explanations.vue'

export default {
  name: 'App',
  components: {
    Introduction,
    Causes,
    Explanations
  }
}
</script>

    