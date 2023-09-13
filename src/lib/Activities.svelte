<script lang="ts">
const platforms =
[
'User Interface Change',
'Visual Design',
'FED/AEM Integration',
'FED/CDS Integration',
'Typescript Development',
'Javascript Development',
'Java Development',
'QA Testing',
'Perf Testing',
'License Change',
'Infrastructure Change',
    'Architecture Change',
    'New Environment',
'Network Config',
'Change Existing Data Feed',
'New Data Feed',
'New Batch Job',
'New Scheduled Task',
'Data Structure Change']
</script>
<h3>Activities</h3>
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