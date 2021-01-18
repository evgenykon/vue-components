<template>
    <div class="base-tabs-container">
        <div class="tabs">
            <a 
                href="javscript:" 
                v-for="(item, i) in tabs" 
                v-bind:class="{active: current && item.id === current.id}" 
                v-bind:key="'tab-' + i" 
                v-on:click="onClickTab(item)"
            >
                {{item.name}}
            </a>
        </div>
        <div class="tab-box">
            <slot></slot>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        tabs: {
            type: Array,
            default: () => {
                return [];
            }
        },
        defaultTabId: {
            type: Number,
            default: 1
        }
    },
    data() {
        return {
            current: null
        }
    },
    mounted() {
        const def = this.tabs.filter(item => item.id === this.defaultTabId);
        if (def.length > 0) {
            this.current = def[0];
        }
        console.log(def);
    },
    methods: {
        onClickTab(item) {
            this.$emit('change-tab', item);
            this.current = item;
        }
    }
}
</script>

<style lang="scss">
.base-tabs-container {
    &>.tabs {
        padding: 5px;
        a {
            padding: 5px;
            color: #4e4e4e;
            text-decoration: none;
            border-right: 1px solid #ccc;
        }
        a.active {
            color: red;
            text-decoration: underline;
            border: 1px solid rgb(117, 0, 0);
            box-sizing: border-box;
            border-top-left-radius: 5px;
            border-top-right-radius: 5px;
            
        }
        border-bottom: 1px solid #ccc;
    }
    &>.tab-box {
        padding: 5px;
    }
}
</style>