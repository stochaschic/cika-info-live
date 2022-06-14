<svelte:head>
  <title>Home | cika.info</title>
  <meta property="og:title" content="home" />
</svelte:head>

<script>
    import PostCard from "../components/PostCard.svelte";
    import item from "../data/projects.json";
    import Header from "../components/Header.svelte";
    import Modal from "../components/Modal.svelte";
    import Credentials from "../components/Credentials.svelte";
    import TechStack from "../components/TechStack.svelte";
    import About from "../components/About.svelte";
    import BacktoTop from "../components/BacktoTop.svelte";
    import {slide} from 'svelte/transition';


    let isOpenModal=false;

    function openModal() {
        isOpenModal = !isOpenModal;
    }
</script>

<Header/>
<hr>
<a name="sample-projects" >
<div class="section-header">
    Projects <span on:click={openModal}>ⓘ</span>
</div>
<Modal isOpenModal={isOpenModal}  />

<div class="posts-container-grid">
    {#each item as cardItem}
        <PostCard title={cardItem.title} tags={cardItem.tags} useCase={cardItem.useCase} problem={cardItem.problem} slug={cardItem.slug} />
    {/each}
    

</div>
</a>
<hr>
<a name="credentials">
    <div class="section-header">
        Credentials
    </div>
    <Credentials/>
</a>
<hr>
<a name="tech-stack">
<div class="section-header">
    Tech Stack
</div>
<TechStack/>
</a>
<hr>
<a name="about">
<div class="section-header">
    About
</div>
<About/>
</a>

<BacktoTop />

<style>
hr {
    margin: 0vw 1% 0 1vw;
}
.section-header {
    padding: 0vw 1vw 0vw 1vw;
    margin-top: 0.8em;
    font-weight: 500;
    font-size: 2rem;
}

.section-header > span {
    font-weight: 300;
    font-size: 1.5rem;
    vertical-align: baseline;
}

.posts-container-grid {
    padding: 1vw;
    padding-top: 2vh;
    display: flex;
    gap: 3vh;
    flex-wrap: wrap;
    font-size: 110%;
    align-items: flex-end;
    align-content: space-between;
}

@media screen and (max-device-width: 480px) {
    .section-header {
        font-size: 1.2rem;
        /* padding-left: calc(50%); */
        padding-left: calc(1vw );
        padding-top: 1.5vh;
    }

    .section-header > span {
        font-size: 0.9rem;
        vertical-align: baseline;
    }
    .posts-container-grid  {
    font-size: 90%;
    justify-content: center;
    gap:1.5vh;
}
}

</style>
