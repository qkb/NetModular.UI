<template>
  <nm-container>
    <demo />
    <nm-code-preview :code="code" />
  </nm-container>
</template>
<script>
import page from './page.js'
import Demo from './demo'
import code from '!!raw-loader!./demo'
export default {
  name: page.name,
  components: { Demo },
  data() {
    return {
      timer: null,
      code
    }
  },
  created() {
    this.setTabName('标签页示例代码')
  }
}
</script>
