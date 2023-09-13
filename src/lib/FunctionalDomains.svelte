<script lang="ts">
    import {createEventDispatcher} from "svelte";

    const domains =
        ['Browse',
            'Search',
            'Cart',
            'Checkout',
            'Loyalty',
            'Payment',
            'Offers',
            'Marketing',
            'Pricing',
            'Inventory',
            'Fulfillment',
            'Returns',
            'Promotions',
            'Auto Fitment',
            'Auto Service',
            'Product',
            'Customer',
            'Order',
        'Store',
        'Vendor',
        'Employee',
        'Supplier',
        'Partner',
        'Technology']
    const dispatcher = createEventDispatcher();

</script>
<h3>Business Domain</h3>
<ul>
{#each domains as domain, index}
    <li>
        <input type="checkbox" id="domain_{index}" on:change={(e)=>dispatcher('notify', {checked: e.srcElement.checked, id: 'domain_' + index, value: domain})} value="{domain}"/>
        <label>{domain}</label>
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