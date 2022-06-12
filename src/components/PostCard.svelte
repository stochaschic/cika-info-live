<script>
import CategoryPill from "./CategoryPill.svelte";

    export let title = '',
               slug = '',
               useCase = '',
               problem = '',
               tags = '';
</script>


<div class="table">
    <div class="row header">
        <div class="cell">
            <a href="projects/{slug}">{title}</a>
        </div>
       
    </div>
    <div class="row">
        <div class="cell">
            <b>Use case</b>
        </div>
        <div class="cell">
            {useCase}
        </div>
    </div>
    <div class="row">
        <div class="cell">
            <b>Problem</b>
        </div>
        <div class="cell">
            {problem}
        </div>
    </div>
    <div class="row">
        <CategoryPill buttonIds={tags}/>       
    </div>
</div>


<style>
    .table {
        flex: 0 1 21%;
    }
    .row {
        display: flex;
        border-bottom: 1px solid #000;
        padding: 1ch 0;
        
    }

    .row > *:nth-child(1) {
        flex: 1 1 30%;
        min-width: 10ch;
    }
    .row > *:nth-child(2) {
        flex: 1 1 70%;
        min-width: 25ch;

    }
    .table > *:nth-child(3) {
        min-height: 5rem;
    }
    .table > *:nth-child(4) {
        border-bottom: none;

    }

    a {
        color: #2C69C6;
        font-weight: 600;
        text-decoration: none;
    }

    a:hover {
        text-decoration: underline;
    }

    a:focus {
        text-decoration: underline;
    }

    @media screen and (max-device-width: 480px) {
        .table > *:nth-child(3) {
            min-height: 4rem;
        }

        .table {
        flex: 0 1 100%;
    }
    }

</style>