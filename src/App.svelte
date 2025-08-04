<script>
    import Icon from "@iconify/svelte";

</script>

<header>
    <h1 class="title">List of Fighters</h1>
</header>
<main>

    <section class="favouriteF">
        <h2 class="favouriteF__titleFavouriteFighters">Favourite Fighters</h2>

        <article class="favouriteF__listFighters">

            <div class="favouriteF__imageBox">
                <img class="favouriteF__FaceImg" src="https://media.gettyimages.com/id/482283375/fr/photo/albuquerque-nm-ufc-lightweight-champion-jon-bones-jones-interacts-with-media-during-an-open.jpg?s=612x612&w=0&k=20&c=lgMiNYuPD2C3m5QBnhsRNSLF5jFE9VTKfymhK_3sdew=" alt="fighter face">
            </div>

            <div class="favouriteF__name-rating">
                <h3>Jon Jones</h3>
                <p>rating : </p>
            </div>

                <Icon icon="mi:calendar" width="24" height="24" />
                <Icon icon="mi:delete" width="24" height="24" />
            
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
        display: flex;
        justify-content: center;
        font-family: 'Bebas Neue', sans-serif;
    }

    main{
        height: 85vh;
        width: 700px;
        display: flex;
        flex-direction: column;
    }

    .title{
        font-size: 4rem;
        font-weight: 700;
        text-transform: uppercase;
        text-align: center;
    }


    .favouriteF{
        border: solid 1px var(--borderClary);
    }


    .favouriteF__titleFavouriteFighters{
        text-transform: uppercase;
        padding: 0.2rem 1rem;
    }

    
    .favouriteF__listFighters{
        display: flex;
        align-items: center;
    }


    

    .favouriteF__imageBox .favouriteF__FaceImg{
        width: 120px;
        height: 100px;
        object-fit: cover;
        object-position: -30px 0;
        border: solid 3px var(--borderClary);
        border-radius: 100%;
        margin: 1rem;
    }

</style>
