<script>
    import { linear } from "svelte/easing";


export let valueProgressBar = 0;

function progressBarColor(value){
    if(value < 33){
        return "linear-gradient(to right, #00ff00, #7fff00)";
    }else if(value < 66){
        return "linear-gradient(to right, #90ff27, #ffcc00)";
    }else{
        return "linear-gradient(to right,#d7ff27, #ff9408, #ff4500)";
    }
}


</script>

<div class="progressBarContainer" >
    
    <div class="progressBar" style="width: {valueProgressBar}%; background:{progressBarColor(valueProgressBar)}"></div>

</div>

<style>

.progressBarContainer{
    width: 200px;
    height: 8px;
    background: #5a5a5a;
    border-radius: 0 10px 10px 0;
    overflow: hidden;
}

.progressBar  {
    height: 100%;
    background: linear-gradient(to right,#d7ff27 ,#ff9408 ); 
    transition: width 0.8s ease;  
    }

</style>