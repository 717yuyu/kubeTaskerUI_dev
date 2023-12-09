<template>

  <div>数据分析</div>
  <Basic :foo="foo">
    <div>
      children内容
    </div>
  </Basic>
</template>

<script lang='ts'>
import { ref, defineComponent } from 'vue'
import {applyReactInVue, applyPureReactInVue} from 'veaury'
import {WorkflowDrawer} from '/root/kubeTaskerUI/src/app/workflows/components/workflow-drawer/workflow-drawer'

export default defineComponent({
  components: {
    Basic: applyReactInVue(WorkflowDrawer)
  },
  setup() {
    const foo = ref('Hello!')

    return {
      foo
    }
  }
})
</script>
<style scoped>

</style>