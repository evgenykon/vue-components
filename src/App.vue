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
                <td>Language selector - default</td>
                <td>
                    <pre>&lt;language-selector&gt;&lt;/language-selector&gt;</pre>
                </td>
                <td>
                    <base-language-selector default="en"></base-language-selector>
                    <base-language-selector default="ru"></base-language-selector>
                </td>
            </tr>
        </table>
        
    </article>
</template>

<script>
import BaseLanguageSelector from './components/BaseLanguageSelector.vue';
export default {
    name: 'App',
    components: {
        BaseLanguageSelector
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
      }
    }
}
</style>