<script context="module" lang="ts">
    export type ContactInfo = {
        link: string;
        name: string;
        iconLink: string;
    };
</script>

<script lang="ts">
    export let contactInfo: ContactInfo[];
</script>

<div id="contact-container">
    <h2 class="grid-header">Kontakt</h2>

    {#each contactInfo as c}
        <div class="img-cont">
            <img class="logo" src={c.iconLink} alt={c.name} style="vertical-align:middle" />
        </div>
        <div class="link-cont">
            <a href={c.link}>{c.name}</a>
        </div>
    {/each}
</div>

<style>
    #contact-container {
        width: 65%;
        margin: 0 auto;
        margin-bottom: 30px;
        
        border-style: solid;
        border-width: 0.13em;
        border-radius: 15px;
        
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: 35px 35px 35px;

        grid-column-gap: 10px;
        grid-row-gap: 5px;
        align-items: center;
    }

    @media screen and (min-width: 1024px) {
        #contact-container {
            width: 30%;
        }
    }
    
    .grid-header{
        margin-top: 1;
        grid-column-start: 1;
        grid-column-end: 4;
    }

    .img-cont {
        grid-column-start: 1;
        grid-column-end: 2;
        justify-self: end;
    }

    .link-cont {
        grid-column-start: 2;
        grid-column-end: 4;
        justify-self: start;
    }
</style>
