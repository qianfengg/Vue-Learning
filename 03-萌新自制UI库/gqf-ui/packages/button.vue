<template>
  <button @click="handleClick" :disabled="disabled" class="gqf-button" :class="[`gqf-button--${type}`, {'is-plain': plain}, {'is-round': round}, {'is-circle': circle}, {'is-disabled': disabled}]">
    <i class="fa" :class="icon" v-if="icon"></i>
    <span v-if="$slots.default">
      <slot></slot>
    </span>
  </button>
</template>

<script>
export default {
  name: 'GqfButton',
  // props: ['type'],
  props: {
    type: {
      type: String,
      default: 'default'
    },
    plain: {
      type: Boolean,
      default: false
    },
    round: {
      type: Boolean,
      default: false
    },
    circle: {
      type: Boolean,
      default: false
    },
    disabled: {
      type: Boolean,
      default: false
    },
    icon: {
      type: String,
      default: ''
    }
  },
  created () {
    // console.log(this.type)
    // console.log(this.$slots, this.$slots.default)
  },
  methods: {
    handleClick (e) {
      this.$emit('click', e)
    }
  }
}
</script>

<style lang="scss" scoped>
.gqf-button {
  display: inline-block;
  line-height: 1;
  white-space: nowrap;
  cursor: pointer;
  background: #fff;
  border: 1px solid #dcdfe6;
  color: #606266;
  -webkit-appearance: none;
  text-align: center;
  box-sizing: border-box;
  outline: none;
  margin: 0;
  transition: 0.1s;
  font-weight: 500;
  -moz-user-select: none;
  -webkit-user-select: none;
  -ms-user-select: none;
  padding: 12px 20px;
  font-size: 14px;
  border-radius: 4px;
  &:hover,
  &:focus {
    color: #409cff;
    border-color: #c6e2ff;
    background-color: #ecf5ff;
  }
}
// type样式
.gqf-button--primary{
  color: #fff;
  background-color: #409eff;
  border-color: #409eff;
  &:hover,
  &:focus {
    background-color: #66b1ff;
    border-color: #66b1ff;
    color: #fff;
  }
}
.gqf-button--success{
  color: #fff;
  background-color: #67c23a;
  border-color: #67c23a;
  &:hover,
  &:focus {
    background-color: #85ce61;
    border-color: #85ce61;
    color: #fff;
  }
}
.gqf-button--info{
  color: #fff;
  background-color: #909399;
  border-color: #909399;
  &:hover,
  &:focus {
    background-color: #a6a9ad;
    border-color: #a6a9ad;
    color: #fff;
  }
}
.gqf-button--warning{
  color: #fff;
  background-color: #e6a23c;
  border-color: #e6a23c;
  &:hover,
  &:focus {
    background-color: #ebb563;
    border-color: #ebb563;
    color: #fff;
  }
}
.gqf-button--danger{
  color: #fff;
  background-color: #f56c6c;
  border-color: #f56c6c;
  &:hover,
  &:focus {
    background-color: #f78989;
    border-color: #f78989;
    color: #fff;
  }
}

// plain样式
.gqf-button.is-plain{
  &:hover,
  &:focus{
    background-color: #fff;
    border-color: #409eff;
    color: #409eff;
  }
}
.gqf-button--primary.is-plain{
  color: #409eff;
  background: #ecf5ff;
  border-color: #b3d8ff;
  &:hover,
  &:focus{
    background: #409eff;
    border-color: #409eff;
    color: #fff;
  }
}
.gqf-button--success.is-plain{
  color: #67c23a;
  background: #f0f9eb;
  border-color: #c2e7b0;
  &:hover,
  &:focus{
    background: #67c23a;
    border-color: #67c23a;
    color: #fff;
  }
}
.gqf-button--info.is-plain{
  color: #909399;
  background: #f4f4f5;
  border-color: #d3d4d6;
  &:hover,
  &:focus{
    background: #909399;
    border-color: #909399;
    color: #fff;
  }
}
.gqf-button--warning.is-plain{
  color: #e6a23c;
  background: #fdf6ec;
  border-color: #f5dab1;
  &:hover,
  &:focus{
    background: #e6a23c;
    border-color: #e6a23c;
    color: #fff;
  }
}
.gqf-button--danger.is-plain{
  color: #f56c6c;
  background: #fef0f0;
  border-color: #fbc4c4;
  &:hover,
  &:focus{
    background: #f56c6c;
    border-color: #f56c6c;
    color: #fff;
  }
}

// 圆角按钮
.gqf-button.is-round{
  border-radius: 20px;
  padding: 12px 23px;
}

// 圆形按钮
.gqf-button.is-circle{
  border-radius: 50%;
  padding: 12px;
}

// 禁用
.gqf-button.is-disabled{
    color: #c0c4cc;
    cursor: not-allowed;
    background-image: none;
    background-color: #fff;
    border-color: #ebeef5;
  &:hover,
  &:focus{
    color: #c0c4cc;
    cursor: not-allowed;
    background-image: none;
    background-color: #fff;
    border-color: #ebeef5;
  }
}

.gqf-button--primary.is-disabled{
    color: #fff;
    background-color: #a0cfff;
    border-color: #a0cfff;
  &:hover,
  &:focus{
    color: #fff;
    background-color: #a0cfff;
    border-color: #a0cfff;
  }
}

.gqf-button--success.is-disabled{
    color: #fff;
    background-color: #b3e19d;
    border-color: #b3e19d;
  &:hover,
  &:focus{
    color: #fff;
    background-color: #b3e19d;
    border-color: #b3e19d;
  }
}

.gqf-button--info.is-disabled{
    color: #fff;
    background-color: #c8c9cc;
    border-color: #c8c9cc;
  &:hover,
  &:focus{
    color: #fff;
    background-color: #c8c9cc;
    border-color: #c8c9cc;
  }
}

.gqf-button--warning.is-disabled{
    color: #fff;
    background-color: #f3d19e;
    border-color: #f3d19e;
  &:hover,
  &:focus{
    color: #fff;
    background-color: #f3d19e;
    border-color: #f3d19e;
  }
}

.gqf-button--danger.is-disabled{
    color: #fff;
    background-color: #fab6b6;
    border-color: #fab6b6;
  &:hover,
  &:focus{
    color: #fff;
    background-color: #fab6b6;
    border-color: #fab6b6;
  }
}

// 处理文字和图标都传的样式
.gqf-button [class*='fa'] + span{
  margin-left: 5px;
}
</style>
