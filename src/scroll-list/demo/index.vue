<template>
  <demo-section>
    <demo-block title="基础用法">
      <scroll-list style="height: 300px" :list="[1, 2, 3, 4, 5]">
        <template #default="scope">
          data: {{ scope.row }} isCur: {{ scope.isCur }}
        </template>
      </scroll-list>
    </demo-block>
    <demo-block title="鼠标进入暂停">
      <scroll-list
        style="height: 300px"
        :list="[1, 2, 3, 4, 5]"
        pause-on-mousein
      >
        <template #default="scope"> data: {{ scope.row }} </template>
      </scroll-list>
    </demo-block>
  </demo-section>
</template>

<script>
import scrollList from '../index.vue';

export default {
  components: {
    scrollList,
  },
};
</script>
