<script lang="ts" setup>
import { Page } from '@vben/common-ui';

import { Card } from 'ant-design-vue';
</script>

<template>
  <Page
    description="使用 micro-app 实现微前端应用加载"
    title="Micro App 微前端演示"
  >
    <Card class="mb-5" title="子应用示例">
      <p class="mb-4">这是一个微前端主应用示例，可以加载其他子应用。</p>
      <!-- 这里可以加载子应用 -->
      <!-- <micro-app 
        name="子应用名称" 
        url="子应用地址"
        :data="dataForChild"
      ></micro-app> -->
      <div class="p-4 bg-gray-100 rounded">
        <p class="text-gray-600">
          配置子应用后，可以在这里展示子应用内容。
        </p>
        <p class="text-gray-600 mt-2">
          子应用需要配置相应的 URL 和名称，然后使用 &lt;micro-app&gt; 标签加载。
        </p>
      </div>
    </Card>
  </Page>
</template>
