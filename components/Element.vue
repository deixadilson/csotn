<template>
  <td v-if="element" colspan="2" class="element">{{ element.replace(/,/g,' ') }}</td>
  <td v-else colspan="2" class="none">None</td>
</template>

<script>
  export default {
    props: ['element']
  }
</script>