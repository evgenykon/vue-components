<template>
  <article class="page">
        <h1>Components</h1>
        <table>
            <tr>
                <th>Name</th>
                <th>Code</th>
                <th>Sample</th>
            </tr>
            <tr>
                <td>Language selector</td>
                <td>
                    <pre>&lt;language-selector default="en"&gt;&lt;/language-selector&gt;</pre>
                </td>
                <td>
                    <base-language-selector default="en"></base-language-selector>
                    <base-language-selector default="ru"></base-language-selector>
                </td>
            </tr>
            <tr>
              <td>Tabs</td>
              <td>
                <pre>
&lt;base-tabs 
  :tabs="[{id: 1, name: "Sample tab 1"}, {id: 1, name:"Sample tab2"}]" 
  :default-tab-id="1"&gt;
    tabs body with if-s
&lt;/base-tabs&gt;
                </pre>
              </td>
              <td>
                <base-tabs 
                  v-bind:tabs="[{id: 1, name:'Sample tab 1'}, {id: 2, name:'Sample tab 2'}]"
                  v-bind:default-tab-id="1"
                  v-on:change-tab="onChangeTab"
                >
                  <p v-if="tab && tab.id === 1">Tab number 1</p>
                  <p v-if="tab && tab.id === 2">Tab number 2</p>
                </base-tabs>
              </td>
            </tr>
        </table>
        
    </article>
</template>

<script>
import BaseLanguageSelector from './components/BaseLanguageSelector.vue';
import BaseTabs from './components/BaseTabs.vue';

export default {
    name: 'App',
    components: {
        BaseLanguageSelector, BaseTabs
    },
    data() {
      return {
        tab: null
      }
    },
    methods: {
      onChangeTab(tab) {
        this.tab = tab;
      }
    }
}
</script>


<style lang="scss" scoped>
article.page {
    font-family: Arial, Helvetica, sans-serif;
    & > table {
        width: 100%;
        & > tr {
            & > td:first-child {
                min-width: 200px;
                width: 20%;
                max-width: 300px;
            }
            & > td:last-child {
                min-width: 500px;
                width: 50%;
            }
        }
    }
    pre {
        background-color: #ececec;
        padding: 0.5rem;
        line-height: 1rem;
        text-align: left;
        border: 1px solid #ccc;
    }
    &>table {
      border: 1px solid #ccc;
      td {
        border: 1px solid #ccc;
        padding: 3px;
        vertical-align: text-top;
      }
    }
}
</style>