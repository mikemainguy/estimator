<script lang="ts">
    import DataTable, { Head, Body, Row, Cell } from '@smui/data-table';
    import Slider from '@smui/slider';
    import Button from '@smui/button';
    import Select, { Option } from '@smui/select';
    type Item = {
        id: number;
        platform: string;
        domain: string;
        component: string;
        size: string;
    };
    let choices = ['Small', 'Medium', 'Large', 'Extra Large'];
    let items: Item[
        ] = [
        {id: 1, domain: 'Search', platform: 'Hybris', component: 'Fed Interaction', size: 'Large'},
    ];
    let value=1;
    const valueMap = [
        'Small',
        'Medium',
        'Large',
        'Extra Large'
    ]

</script>

<DataTable stickyHeader style="width:100%">
    <Head>
        <Row>

            <Cell>ID</Cell>
            <Cell style="width: 200px; text-align: center">Size</Cell>
            <Cell></Cell>


            <Cell>Domain</Cell>
            <Cell>Platform</Cell>
            <Cell>Component</Cell>
            <Cell></Cell>
        </Row>
    </Head>
        <Body>

            {#each items as item (item.id)}
                <Row>

                    <Cell>{item.id}</Cell>
                    <Cell style="width: 200px; align-content: center">
                        <Slider min={0} bind:value max={3} step={1}  discrete tickMarks/>
                    </Cell>
                    <Cell style="width: 200px">
                        <span style="display: inline-block">{valueMap[value]}</span>
                    </Cell>

                    <Cell>{item.domain}</Cell>
                    <Cell>{item.platform}</Cell>
                    <Cell>{item.component}</Cell>
                    <Cell>
                        <Button>Remove</Button>
                    </Cell>

                </Row>
                {/each}
        </Body>

</DataTable>