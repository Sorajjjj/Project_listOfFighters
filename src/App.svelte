<script>
    import Icon from "@iconify/svelte";
    import ProgressBar from "./componants/ProgressBar.svelte";
    

    const valueRating = 4.5;
    let valueProgressBar = 0;

</script>

<header>
    <h1 class="title">List of FIGHTERS</h1>
</header>
<main>

    <section class="favouriteF">
        <h2 class="favouriteF__titleFavourite">Favourite Fighters</h2>

        <article class="favouriteF__listFighters">

            <div class="favouriteF__imageBox">
                <img class="favouriteF__FaceImg" src="https://media.gettyimages.com/id/482283375/fr/photo/albuquerque-nm-ufc-lightweight-champion-jon-bones-jones-interacts-with-media-during-an-open.jpg?s=612x612&w=0&k=20&c=lgMiNYuPD2C3m5QBnhsRNSLF5jFE9VTKfymhK_3sdew=" alt="fighter face">
            </div>

            <div class="favouriteF__name-rating">
                <h3>Jon Jones</h3>
                <p>Rating : {valueRating} </p>
            </div>

                <div class="favoutiteF__containerCalendar">
                    <div class="favoutiteF__iconCalendar">
                        <Icon icon="mi:calendar" width="60" height="60" />
                    </div>
                    <!-- todo récupérer la valeur des date pour influencer la bar de chargement pour le prochain combat -->
                    <ProgressBar bind:valueProgressBar />
                </div>
                
                <div class="favoutiteF__iconTrash">
                    <Icon icon="meteor-icons:xmark" width="30" height="30"  onclick={(event) => {
                    console.log("je clique sur la barre")
                    valueProgressBar += 10;
                    console.log(valueProgressBar);

                }} />
                </div>
            
        </article>

    </section>


    <section class="addFavouriteF">

        <h2 class="favouriteF__titleFavourite">Add Favourite Fighter</h2>
        <form>
            <span class="addFavouriteF__inputText">
                <input class="addFavouriteF__inputName" type="text" placeholder="Name">
                <input class="addFavouriteF__inputRating" type="text" placeholder="Rating">
            </span>
            <div class="addFavouriteF__formSubmit">
                <button type="submit"> Add Fighter</button>
            </div>
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
        border-radius: 0.5rem;
        height: 60vh;
        
    }


    .favouriteF__titleFavourite{
        text-transform: uppercase;
        padding: 0.3rem 1rem;
    }

    .favouriteF__listFighters{
        display: flex;
        background-color: var(--secondaryColoryVariant);
        align-items: center;
        border-bottom: solid 1px var(--borderClary);
        border-top: solid 1px var(--borderClary);
    }

    /* icon */
    .favoutiteF__iconCalendar{
        
        position: relative;
        left: -7px;
        
        
    }

    .favoutiteF__containerCalendar{
        position: relative;
        left: 150px;
    }

    


    .favoutiteF__iconTrash{
        position: relative;
        left: -390px;
        top: 35px;
        rotate: 10px;
        
        
        
    }

    .favouriteF__imageBox .favouriteF__FaceImg{
        width: 110px;
        height: 90px;
        object-fit: cover;
        object-position: -30px 0;
        border: solid 3px var(--borderClary);
        border-radius: 100%;
        margin: 1rem;
    }

    .favouriteF__name-rating{
        font-size: 1.3rem;
    }

    .favouriteF__name-rating h3{
        text-transform: uppercase;
    }

    
/* section Add Favourite Fighter */
    .addFavouriteF{
        
        margin: 2rem 0 0 0;
        border: solid 1px var(--borderClary);
        border-radius: 0.5rem;
    }

    .addFavouriteF__inputText{
        display: flex;
        justify-content: center;   
    }

    .addFavouriteF__inputText input[type="text"]{
        width: 100%;
        height: 2.3rem;
        background-color: var(--primaryColor);
        color: var(--textColor);
        border: solid 1px var(--borderClary);
    }

    .addFavouriteF__inputName{
        margin: 0 0.1rem 0 1rem;
        border-radius: 8px 0 0 8px;
        
    }

    .addFavouriteF__inputRating{
        margin: 0 1rem 0 0.1rem;
        border-radius: 0 8px 8px 0;
    }




    .addFavouriteF__formSubmit button[type="submit"]{
        border: solid 1px var(--borderClary);
        background-color: var(--secondaryColoryVariant);
        color: var(--textColor);
        
        height: 4rem;
        border-radius: 8px;
        width: 95%;
        text-transform: uppercase;
        font-weight: 700;
        font-size: 2rem;
        margin: 1rem;
        
    }

</style>
