<template>
  <div id="app">
<!--     <h2>输入框</h2>
    <div>
      <t-input v-model="input" value="123">
        <t-icon slot="prefix" name="close-o" />
        <t-icon slot="suffix" name="close-o" />
        <template slot="before">http://</template>
        <template slot="after">.com</template>
      </t-input>
    </div>
    <div>
      <t-input v-model="input" prefix-icon="share" value="123" suffix-icon="share">
        <template slot="before">http://</template>
        <template slot="after">.com</template>
      </t-input>
    </div>
    <div>
      <t-input v-model="input" prefix-icon="share" value="123" show-password>
        <template slot="before">http://</template>
        <template slot="after">.com</template>
      </t-input>
    </div>
    <div class="row demo-input-addon">
      <t-input v-model="input" value="123">
        <template slot="before">http://</template>
      </t-input>
      <br>
      <br>
      <t-input v-model="input" value="123">
        <template slot="after">.com</template>
      </t-input>
      <br>
      <br>
      <t-input v-model="input" value="123">
        <template slot="before">http://</template>
        <template slot="after">.com</template>
      </t-input>
    </div>
    <div class="row demo-input">
      <t-input v-model="input" value="123" />
      <t-input v-model="input4" placeholder="请输入内容" />
      <t-input disabled placeholder="请输入内容" />
      <br>
      <br>
      <t-input v-model="input2" show-password class="show-password-demo" />
      <t-input v-model="input3" clearable />

      <p>{{ 'input：' + input }}</p>
      <p>{{ 'input2：' + input2 }}</p>
      <p>{{ 'input3：' + input3 }}</p>
      <p>{{ 'input4：' + input4 }}</p>
      <div>
        <t-input v-model="input5" type="textarea" placeholder="请输入内容" />
        <p>{{ 'input5：' + input5 }}</p>
      </div>
    </div> -->
    <h2>按钮</h2>
    <div class="row">
      <span class="label">英文：</span>
      <t-button>Default</t-button>
      <t-button type="primary">Primary</t-button>
      <t-button error>Error</t-button>
      <t-button type="primary" error>Error</t-button>
    </div>
    <div class="row">
      <span class="label">普通按钮：</span>
      <t-button>默认按钮</t-button>
      <t-button type="primary">主要按钮</t-button>
      <t-button error>警告按钮</t-button>
      <t-button type="primary" error>警告按钮</t-button>
    </div>
    <div class="row">
      <span class="label">Icon 按钮：</span>
      <t-button icon="search">默认按钮</t-button>
      <t-button type="primary" icon="calendar">主要按钮</t-button>
      <t-button icon="share" error>警告按钮</t-button>
      <t-button type="primary" icon="calendar-dates" error>警告按钮</t-button>
    </div>
    <div class="row">
      <span class="label">禁用状态：</span>
      <t-button disabled>默认按钮</t-button>
      <t-button type="primary" disabled>主要按钮</t-button>
      <t-button error disabled>警告按钮</t-button>
      <t-button type="primary" error disabled>警告按钮</t-button>
    </div>
    <div class="row">
      <span class="label">Loading 按钮：</span>
      <t-button loading>默认按钮</t-button>
      <t-button type="primary" loading>主要按钮</t-button>
      <t-button loading error>警告按钮</t-button>
      <t-button type="primary" loading error>警告按钮</t-button>
    </div>
    <h2>按钮组</h2>
    <div class="row button-group">
      <t-button-group style="margin-right: 20px; margin-bottom: 20px;">
        <t-button>上一页</t-button>
        <t-button>当前页</t-button>
        <t-button>下一页</t-button>
      </t-button-group>
      <t-button-group style="margin-right: 20px; margin-bottom: 20px;">
        <t-button type="primary">上一页</t-button>
        <t-button type="primary">当前页</t-button>
        <t-button type="primary">下一页</t-button>
      </t-button-group>
      <t-button-group style="margin-right: 20px; margin-bottom: 20px;">
        <t-button error>上一页</t-button>
        <t-button error>当前页</t-button>
        <t-button error>下一页</t-button>
      </t-button-group>
      <t-button-group style="margin-right: 20px; margin-bottom: 20px;">
        <t-button type="primary" error>上一页</t-button>
        <t-button type="primary" error>当前页</t-button>
        <t-button type="primary" error>下一页</t-button>
      </t-button-group>
      <t-button-group />
    </div>
    <!-- <h2>倒计时</h2>
    <div class="row">
      <span class="label">倒计时按钮：</span>
      <t-countdown
        ref="countdown"
        prompt="秒后重新发送"
        :begin-second="5"
        @count-start="isCount = true"
        @count-end="isCount = false"
        @click="clickCount"
      />
    </div>
    <h2>Icon 图标</h2>
    <div class="row icon-list">
      <span class="label">Icon 组件：</span>
      <t-icon name="alarm" />
      <t-icon name="aspect-ratio" />
    </div> -->

  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
  },
  data() {
    return {
      isLoading: true,
      isCount: false,
      input: '我是input',
      input2: '我是input',
      input3: '我是input',
      input4: '',
      input5: ''
    }
  },
  methods: {
    clickCount() {
      if (!this.isCount) {
        this.$refs['countdown'].startCount()
      }
    }
  }
}
</script>

<style>
#app {
  width: 670px;
  margin: 0 auto;
  padding: 0 20px;
  font-family: Helvetica Neue,Helvetica,PingFang SC,Hiragino Sans GB,Microsoft YaHei,SimSun,sans-serif;
}
h2 {
  text-align: center;
}

.row {
  margin: 20px 0;
}
.row:not(.button-group) button {
  margin-right: 15px;
}
.icon-list > [class^="t-icon-"] {
  margin-right: 20px;
}
.label {
  text-align: right;
  width: 120px;
  display: inline-block;
  padding-right: 10px;
}
</style>
