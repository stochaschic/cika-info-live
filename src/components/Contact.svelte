<!-- src/Modal.svelte -->
<script>
    import { createEventDispatcher } from 'svelte';
	
    const dispatch = createEventDispatcher();
	
    export let isOpenModal;
	
    function closeModal() {
        isOpenModal = false;
        dispatch('closeModal', { isOpenModal });
    }
</script>

<div id="background" style="--display: {isOpenModal ? 'block' : 'none'};" on:click={closeModal}></div>
<div id="name-card" style="--display: {isOpenModal ? 'block' : 'none'};">
    <p id="phone-number">ask@cika.info</p>
    <div id="company-section">
        <p id="company">Cika & Cika</p>
        <p id="murders-and-executions">Queries And Executions</p>
    </div>
    <div id="name-and-title">
        <div id="names">
            <p id="first-name">Rizka</p>
            <p id="last-name">Azmira</p>
        </div>
        <p id="title">Data Scientist</p>
    </div>
    <p id="bottom-info">Jakarta, Indonesia (But Willing to Relocate)</p>
    <p></p>
</div>


<style>
    p {
        font-size: calc(480/350 * 0.95em);
        margin: 0;
    }
    #background {
        display: var(--display);
        position: fixed;
        z-index: 1;
        top: 0;
        left: 0;
        width: 100vw;
        height: 100vh;
    }

    #name-card {
        display: var(--display);
       	position: fixed;
        z-index: 2;
        top: calc(50%);
        left: 50%;
        transform: translate(-50%, -50%);
        background: #e3dac9;
        border: 1px solid black;    
        width: 480px;
        height: calc(20/35 * 480px);
        text-transform: uppercase;

    }

    #first-name {
        font-size: calc(480/350 * 0.75em);
  
    }
    #last-name {
        font-size: calc(480/350 * 0.9em);
    }
    #title {
        font-size: calc(480/350 * 0.76em);
    }

    #phone-number {
        font-size: calc(480/350 * 0.85em);
        position: absolute;
        top: calc((20/35 * 480)/200 * 20px);
        left: calc(480/350 * 25px);
        text-transform: lowercase;
    }

    #murders-and-executions {
	    font-size: calc(480/350 * 0.52em);
    }
    
    
        #company-section > *:nth-child(1) {
            margin-bottom: 0;
        }
        #company-section > *:nth-child(2) {
            margin-top: 0;
        }
    #company-section {
        position: absolute;
        top: calc((20/35 * 480)/200 * 20px);
        right: calc(480/350 * 25px);
    }

    #name-and-title {
	position: absolute;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
}

#first-name {
	display: inline-block;
}
#last-name {
	display: inline-block;
}
#title {
	text-align: center;
	font-size: calc(480/350 * 0.8em);
}
#bottom-info {
	position: absolute;
	bottom: 0;
	left: 0;
	right: 0;
	text-align: center;
	font-size: calc(480/350 * 0.60em);
	padding: 10px;
}
    @media screen and (max-device-width: 480px) {
        #name-card {
            width: 80%;
            height: calc(20/35 * 0.8 * 100vw);
        }
    }

    </style>