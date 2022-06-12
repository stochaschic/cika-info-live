<script>
 let buttonList = [
		{ id: 'causal_inf', name: 'Causal Inference', buttonColor: '#FEFFCE' },
        { id: 'propensity_modeling', name: 'Propensity Modeling', buttonColor: '#CEFFF3'},
        { id: 'product_analytics', name: 'Product Analytics', buttonColor: '#CEF0FF'},
        { id: 'segmentation', name: 'Segmentation', buttonColor: '#FFCED1'},
		{ id: 'spatial', name: 'Spatial Analytics',  buttonColor: '#E4FFCE'  },
        { id: 'crm', name: 'CRM', buttonColor: '#FFF'},
        { id: 'analysis', name: 'Analysis', buttonColor: '#fff'},
        { id: 'credit_risk', name: 'Credit Risk', buttonColor: '#fff'},
        { id: 'production_ml', name: 'Production ML', buttonColor: '#fff'},
        { id: 'software', name: 'Software', buttonColor: '#fff'}
	];
    export let buttonIds = ['causal_inf']
    buttonList = buttonList.filter(i => buttonIds.includes(i.id))


</script>

<div class="pills">
{#each buttonList as buttonItem}
    <button style="background-color:{buttonItem.buttonColor};">{buttonItem.name}</button>
{/each}
</div>



<style>
    .pills {
        display: flex;
        flex-wrap: wrap;
        
    }

    .pills > * {
        flex-grow: 1;
        flex-shrink: 1;

    }

    button {
        border: 1px solid black;
        color: black;
        padding: 5px 10px;
        text-align: center;
        text-decoration: none;
        font-family: 'Work Sans', sans-serif;
        font-weight: 500;
        display: inline-block;
        margin: 3px 2px;
        border-radius: 28px;


        }

 


  
</style>