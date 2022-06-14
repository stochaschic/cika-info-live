<script>
    import Contact from './Contact.svelte';

    const buttonList = [
        { name: 'Contact', buttonColor: '#e3dac9', textColor: '#000', linkTo: "" },
        { name: 'Projects', buttonColor: '#000', textColor: '#FFF', linkTo: "#sample-projects" },
        { name: 'Credentials', buttonColor: '#000', textColor: '#fff', linkTo: '#credentials' },
        { name: 'Tech Stack', buttonColor: '#000', textColor: '#fff', linkTo: '#tech-stack' },
        { name: 'About', buttonColor: '#000', textColor: '#fff', linkTo: '#about' },
       ];


       let isOpenModal = false;

        function openModal() {
            isOpenModal = true;
        }

        function closeModal() {
            isOpenModal = false;
        }
   </script>
   
   <Contact  isOpenModal={isOpenModal} on:closeModal={closeModal} />

   <div class="pills">
   {#each buttonList as buttonItem}
   {#if buttonItem.name == 'Contact'}
   <a href="{buttonItem.linkTo}" on:click={openModal}  style="background-color:{buttonItem.buttonColor};color:{buttonItem.textColor}">{buttonItem.name}</a>
   {:else}
   <!-- svelte-ignore a11y-missing-attribute -->
   <a href="{buttonItem.linkTo}" style="background-color:{buttonItem.buttonColor};color:{buttonItem.textColor}">{buttonItem.name}</a>
   {/if}
   {/each}
   </div>
   
   
   
   <style>
       .pills {
           display: flex;
           flex-wrap: wrap;
           gap: 0.01em;
           
       }
   
       .pills > * {
           flex-grow: 0;
           flex-shrink: 1;
           font-weight: 500;
   
       }

       .pills > *:nth-child(1) {
           
           
           min-width: 4rem;
        }
        .pills > *:nth-child(2) {

            min-width: 3rem;
       }
        .pills > *:nth-child(5) {
            flex-basis: 5%;
            flex-shrink: 1;
       }
   
       a {
           border: 1px solid black;
           color: black;
           padding: 5px 10px;
           text-align: center;
           text-decoration: none;
           display: inline-block;
           margin: 3px 2px;
           font-size: 0.8rem;
   
   
           }
   
           .pills {
               margin: 0.7em 0;
           }
    
    @media screen and (max-device-width: 480px) {
        .pills > *:nth-child(1) {
            flex-grow: 1;
            flex-basis: 100%;
            max-width: 13rem;
        }
        .pills > *:nth-child(2) {
            max-width: none;
            flex-grow: 1;

       }
        .pills > * {
            flex-grow: 1;
        }

    }
     
   </style>