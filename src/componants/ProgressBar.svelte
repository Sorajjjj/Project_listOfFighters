<script>

export let valueProgressBar = 0;


</script>

<div class="progressBarContainer" >
    
    <div class="progressBar" style="width: {valueProgressBar}%"></div>
    <!-- <h4>le compenant marche</h4> -->

</div>

<style>

.progressBarContainer{
    width: 200px;
    height: 10px;
    background: #5a5a5a;
    border-radius: 10px;
}

.progressBar  {
    height: 100%;
    background: linear-gradient(to right, #ff4747, #ff9d47); 
    transition: width 0.3s ease;  
    }

</style>