<template>
  <div>
    <h1>ToDoリスト</h1>
    <br />
    <Radio />
    <br />
    <Table />
    <br />
    <h2>新規タスクの追加</h2>
    <Task />
  </div>
</template>

<script lang="ts">
import { defineComponent, provide } from '@vue/composition-api';
// logic
import taskLogicStore from '@/composables/store/taskLogic';
// key
import taskLogicKey from '@/composables/key/taskLogicKey';
// components
import Radio from '@/components/Radio.vue';
import Table from '@/components/Table.vue';
import Task from '@/components/Task.vue';

export default defineComponent({
  components: { Radio, Table, Task },
  setup() {
    provide(taskLogicKey, taskLogicStore());
  },
});
</script>

<style></style>
