<script lang="ts">
  import FunctionalDomains from './lib/FunctionalDomains.svelte';
  import PlatformsComponents from "./lib/PlatformsComponents.svelte";
  import Function from "./lib/Function.svelte";
  import EstimatorGrid from "./lib/EstimatorGrid.svelte";
  import LayoutGrid, { Cell } from '@smui/layout-grid';
  import Activities from "./lib/Activities.svelte";
  import Select, {Option} from '@smui/select';
  function handleMessage(event) {
    console.log('event' + JSON.stringify(event.detail));
  }
</script>
<header>
  Estimator
</header>
<main>

  <LayoutGrid>
    <Cell span="{12}">
      <h2>Strategic Theme</h2>
      Strategic themes are portfolio-level business objectives that provide competitive differentiation and strategic advantage. They provide business context for portfolio strategy and decision-making, representing aspects of the enterprise’s strategic intent.
    </Cell>
    <Cell span="{12}">
      <Select style="width: 100%">
        <Option>Customer-Centric Experience Enhancement</Option>
        <Option>Supply Chain Optimization</Option>
        <Option>E-commerce Technology and Innovation</Option>
        <Option>Market Expansion and Diversification</Option>
      </Select>
    </Cell>
    <Cell span="{3}">

    </Cell>
    <Cell span="{3}">
      <h3>Objectives</h3>
    </Cell>
    <Cell span="{3}">
      <h3>Key Results</h3>
    </Cell>
    <Cell span="{12}">
      <h2>Value Stream</h2>
      A value stream represents the series of steps and activities that an organization uses to deliver a product or service to its customers. It encompasses all the activities, from the initial idea or concept through development, testing, deployment, and ultimately to the customer's hands. Value streams are typically cross-functional, involving multiple teams and departments, and they cut across organizational boundaries.
    </Cell>
    <Cell span="{12}">
      <Select id="valuestream" style="width: 100%">
        <Option>Omnichannel Customer Experience</Option>
        <Option>Inventory Management and Fulfillment</Option>
        <Option>Customer Engagement and Loyalty</Option>
        <Option>Innovation and Technology Adoption</Option>
      </Select>
    </Cell>

  </LayoutGrid>
  <Function on:message={handleMessage}/>
  <LayoutGrid>
    <Cell span="{4}">
      <FunctionalDomains on:notify={handleMessage}/>
    </Cell>
    <Cell span="{4}">
      <PlatformsComponents />
    </Cell>
    <Cell span="{4}">
      <Activities />
    </Cell>
  </LayoutGrid>
  <EstimatorGrid />

</main>

<style>
  header {
    background-color: #1a202c;
    color: white;
    font-size: 2em;
    padding: 0.5em;
    text-align: center;
  }

</style>
