<div class="wrapper">
    <div class="categ">Data visualization
        <ul>
            <li>
                ggplot2
            </li>
            <li> Tableau </li>
            <li> Google Data Studio </li>
            <li> Svelte </li>
        </ul>
    </div>
    <div class="categ">Data processing & modeling
    <ul>
        <li>R</li>
        <li>SQL</li>
        <li>BigQuery</li>
        <li>Python</li>
        <li>Spark</li>
        <li>MongoDB</li>
    </ul>
</div>
    <div class="categ">Miscellaneous Tech
        <ul>
            <li>Adobe Photoshop</li>
            <li>Figma</li>
            <li>HTML</li>
            <li>CSS</li>
            <li>Svelte</li>
        </ul>
    </div>
</div>

<style>

    .wrapper {
        display: flex;
        padding:1em;
        font-weight: 600;
        flex-wrap: wrap;
    }

    .wrapper > * {
        flex-basis: 33%;
        min-width: 20em;
    }
    ul {
        font-weight: 400;
    }
    li {
        padding: 0.3em;
    }

    @media screen and (max-device-width: 480px) {
        .wrapper {
            padding:1em 1vw;
            font-size: 0.9em;
        }
    }
        
</style>