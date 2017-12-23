<template>
  <div class="main">
    <div
        class="directive-test"
        v-add="color"
    >
      {{num}}
    </div>
    <button @click="add">add</button>
  </div>
</template>

<script>
export default {
    name: 'index',
    data () {
        return {
            num: 1,
            color: '#ff0000',
        }
    },
    directives: {
        add: {
            // 指令第一次绑定到元素时调用
            bind (el, binding, vnode) {
                el.style = 'color:' + binding.value
                console.log('bind...')
            },
            // 被绑定元素插入父节点时调用（
            inserted () {
                console.log('inserted...')
            },
            // 元素所在的模板更新时调用
            update () {
                console.log('update...')
            },
            // 被绑定元素所在模板完成一次更新周期时调用
            componentUpdated () {
                console.log('componentUpdated...')
            },
            // 指令与元素解绑时调用
            unbind () {
                console.log('unbind...')
            }
        }
    },
    methods: {
        add () {
            this.num++
        }
    }
}
</script>

<style scoped>

</style>
