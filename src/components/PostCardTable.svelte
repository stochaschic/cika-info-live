<script>
    export let title = 'Optimal Credit Limit Assignment with Causal Inference',
               link = '',
               useCase = 'Digital lending', 
               problem = 'How to appropriately assign credit limit to new debtors to increase sales volume while keeping risk at bay',
               tags = 'crm,causal_inf,spatial,analysis';
    import CategoryPill from "../components/CategoryPill.svelte";
</script>

<table class="post-wrapper">
    <thead>
        <tr>
            <th colspan="2">{title}</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><b>Use case</b></td>
            <td>{useCase}</td>
        </tr>
        <tr class="active-row">
            <td><b>Problem</b></td>
            <td>{problem}</td>
        </tr>
        <tr>
            <td colspan="2">
                <CategoryPill buttonIds={tags}/>       
            </td>
        </tr>
    </tbody>
</table>

<style>


    .post-wrapper {
        border-collapse: collapse;
        margin: 25px 0;
        font-size: 0.9em;
        font-family: sans-serif;
        min-width: 400px;
        max-width: 400px;
    }

    .post-wrapper thead tr {
    background-color: #009879;
    color: #ffffff;
    text-align: left;
    }

    .post-wrapper th,
    .post-wrapper td {
        padding: 12px 15px;
    }

    .post-wrapper tbody tr {
        border-bottom: 1px solid #000;
    }

    .post-wrapper tbody tr:last-of-type {
        border-bottom: none;
    }

 
</style>