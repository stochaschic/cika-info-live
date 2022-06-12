<script>
    import RoutesPill from "./RoutesPill.svelte";
</script>
<div class="headline-container">
    <div class="name">
        <div class="big">
            Rizka A.
        </div>
        <div class="medium">
            ㋡ 1999 
        </div>
        </div>
    <div class="description small">
        <div class="description-text">
        Rizka is a data professional based in Jakarta, Indonesia with 4+ YOE working across multiple industries (distribution, ride hailing, consumer lending and digital banking). Specialties include product analytics, scorecard development, propensity modeling. 
        </div>
        <div class="description-pills">
            <RoutesPill/>
        </div>
    </div>  
</div>

<style>
    .headline-container {
        display: flex;
        align-items: flex-start;
        flex-wrap:wrap;
    }
    
    .headline-container > *:nth-child(1) {
        min-width: 24rem;
        /* flex: 1 1 50%; */
        /* border: 1px solid black; */
    }
    .headline-container > *:nth-child(2) {
        min-width: 0rem;
        flex-basis: 43%;
        flex-grow: 1;
        flex-shrink: 0;
        /* flex: 1 1 50%; */
        /* padding-right: 10vw; */
        /* padding-left: 1vw; */
        padding: 0vw 5.5% 2vw 1vw;
        /* border: 1px solid black; */
    }
    .name {
        padding: 1vw 1vw;
    }
    .big {    
        font-weight: 600;
        font-size: 4rem;
    }
    .medium {
        font-weight: 400;
        font-size:2rem;
    }

    .small {
        font-weight: 300;
        font-size:1rem;
    }

    .description {
        margin-top: 1.2em;
        margin-bottom: 0em;
    }

@media screen and (max-device-width: 480px) {
    .big {
        font-weight: 600;
        font-size: 3rem;
    }
    .medium {
        font-size: 1.7rem;
    }
    .small {
        font-size: 0.75rem;
    }


}
</style>