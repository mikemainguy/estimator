<script lang="ts">
const platforms =
['Gigya (Identity)',
'Gigya (Profile)',
'AEM Template',
'AEM Component',
'CDS Service',
'Hybris Service',
'Hybris Data',
'Hybris Logic',
'Search (Bloomreach)',
'Product Information (PIM/PCM)',
'Bloomreach',
'Epsilon',]
</script>
<h3>Platforms</h3>
<ul>
    {#each platforms as platform}
        <li>
            <input type="checkbox" value="{platform}"/>
            <label>{platform}</label>
        </li>
    {/each}
    <li>
        <input type="checkbox" value="Other"/>
        <input type="text" placeholder="Other"/>
    </li>
</ul>
<style>
    li {
        list-style-type: none;
        text-align: left;
    }
</style>