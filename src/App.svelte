<script>
    import Icon from "@iconify/svelte";

</script>

<header>
    <h1>List of Fighters</h1>
</header>
<main>

    <section class="favouriteF">
        <h2>Favourite Fighters</h2>

        <article>
            <img src="https://media.gettyimages.com/id/482283375/fr/photo/albuquerque-nm-ufc-lightweight-champion-jon-bones-jones-interacts-with-media-during-an-open.jpg?s=612x612&w=0&k=20&c=lgMiNYuPD2C3m5QBnhsRNSLF5jFE9VTKfymhK_3sdew=" alt="fighter face">
            <div>
                <h3>Jon Jones</h3>
                <p>rating : </p>
                <Icon icon="mi:calendar" width="24" height="24" />
                <Icon icon="mi:delete" width="24" height="24" />
            </div>
        </article>

    </section>


    <section class="addFavouriteF">

        <h2>Add Favourite Fighter</h2>
        <form>
            <div><input type="text" placeholder="Name"></div>
            <div><input type="text" placeholder="Rating"></div>
            <button type="submit"> Add Fighter</button>
        </form>

    </section>





</main>


<style>
    
    /* variable a utiliser

    --primaryColor: #121212;
    --scondaryColor: #2B0A0C;
    --secondaryColoryVariant: #3F0C0B;
    --textColor: #D1C39E;
    --borderClary: #903127;
     */



    :global(body){
        background-color: var(--primaryColor);
        color: var(--textColor);
    }

</style>
