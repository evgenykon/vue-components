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
                    <language-selector></language-selector>
                </td>
            </tr>
        </table>
        
    </article>
</template>

<script>
import LanguageSelector from './components/LanguageSelector.vue';
export default {
    name: 'App',
    components: {
        LanguageSelector
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
        background-color: #fcfcfc;
        padding: 0.5rem;
        line-height: 1rem;
        text-align: left;
    }
}
</style>