<!-- src/Modal.svelte -->
<script>
    export let isOpenModal;

</script>

<div id="modal" style="--display: {isOpenModal ? 'block' : 'none'};">
    <p>Non-exhaustive, details redacted due to confidentiality issues.</p>
</div>

<style>


    #modal {
        display: var(--display);
        position: absolute;
        z-index: 2;
        background-color: #fff;
        border: 1px solid black;
        transform: translate(calc((2 * 8em) + 0.7em),-3.3em);
        /* transform: translate(calc(100% + 3.5em),calc(-100% - 0.3em)); */
        padding-left:1em;
        padding-right: 1em;
        font-size: 0.7em;
        max-width: 50%;
    }

    @media screen and (max-device-width: 480px) {
    #modal {
        transform: translate(calc(0.6 * ((2 * 8em)) + 0.3em),calc(-80% - 0em));
        max-width: 50%;
    }

    #modal > p {
        margin: 0.5em 0;
    }
    }
</style>