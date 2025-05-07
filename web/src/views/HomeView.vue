<template>

    <n-config-provider :theme="theme">
      <n-space vertical size="large">
    <n-layout>
      <n-layout-header>颐和园路</n-layout-header>
      <n-layout-content content-style="padding: 30px;">
        平山道
      </n-layout-content>
      <n-layout-footer>成府路</n-layout-footer>
    </n-layout>

  </n-space>
      <n-card>
        <n-space>
          <n-button @click="theme = darkTheme">
            深色
          </n-button>
          <n-button @click="theme = null">
            浅色
          </n-button>
        </n-space>
      </n-card>
    </n-config-provider>

</template>

<script>
import { darkTheme, NButton, NSpace, NCard, NConfigProvider, lightTheme, NThemeEditor,NLayout,NLayoutContent,NLayoutFooter,NLayoutHeader } from "naive-ui";
import { defineComponent, ref } from "vue";

/**
 * @type import('naive-ui').GlobalThemeOverrides
 */
const blueThemeOverrides = {
  common: {
    primaryColor: '#0000FF'
  },
  Button: {
    textColor: '#0000FF'
  },
  Select: {
    peers: {
      InternalSelection: {
        textColor: '#0000FF'
      }
    }
  }
};

export default defineComponent({
  setup() {
    return {
      darkTheme,
      theme: ref(null),
      blueThemeOverrides
    };
  },
  components: {
    NButton,
    NSpace,
    NCard,
    NConfigProvider,
    NLayout,
    NLayoutContent,
    NLayoutFooter,
    NLayoutHeader
  }
});
</script>
<style scoped>
.n-layout-header,
.n-layout-footer {
  background: rgba(128, 128, 128, 0.2);
  padding: 24px;
}

.n-layout-sider {
  background: rgba(128, 128, 128, 0.3);
}

.n-layout-content {
  background: rgba(128, 128, 128, 0.4);
}
</style>