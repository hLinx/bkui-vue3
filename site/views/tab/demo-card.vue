<template>
  <div>
    <div style="margin-bottom: 15px;">
      <div>
        选项卡样式:
      </div>
      <bk-radio-group v-model="currentType">
        <bk-radio-button
          v-for="item in type"
          :key="item"
          :label="item"
          :value="item"
        >
          {{ item }}
        </bk-radio-button>
      </bk-radio-group>
    </div>
    <div style="margin-bottom: 15px;">
      <div>
        top position:
      </div>
      <bk-radio-group v-model="currentTopPosition">
        <bk-radio-button
          v-for="item in topPosition"
          :key="item"
          :label="item"
          :value="item"
        >
          {{ item }}
        </bk-radio-button>
      </bk-radio-group>
    </div>
    <bk-tab
      v-model:active="active"
      :type="currentType"
      :tabPosition="currentTopPosition"
    >
      <bk-tab-panel
        v-for="(item,index) in panels"
        :key="item.name"
        :name="item.name"
        :label="item.label"
      >
        {{ item.label }}-{{ index }}
      </bk-tab-panel>
    </bk-tab>
  </div>
</template>
<script>
  import { defineComponent } from 'vue';

  export default defineComponent({
    data() {
      return {
        panels: [
          { name: 'mission', label: '任务报表', count: 10 },
          { name: 'config', label: '加速配置', count: 20 },
          { name: 'history', label: '历史版本', count: 30 },
          { name: 'deleted', label: '已归档加速任务', count: 40 },
        ],
        active: 'mission',
        currentType: 'underline',
        currentTopPosition: 'top',
        type: ['underline', 'overline', 'border-block', 'contrast', 'contrast-block', 'capsule'],
        topPosition: ['top', 'right', 'left']
      };
    },
  });
</script>
