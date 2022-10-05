

<script lang="ts">
    // import {IResult} from './interfaces/api.interface'
    let src = "123";

    const fetchDog = () => {
        fetch("https://dog.ceo/api/breeds/image/random")
            .then(res => res.json())
            .then(result => {
                console.log(result)
                src = result.message
            })
            .catch(err => console.log(err))

        // src = fetch("https://dog.ceo/api/breeds/image/random").json
    }
</script>



<div class="half">
    <button on:click={fetchDog}>
        fetch a new dog
    </button>
    <br>
    <img src={src} alt="random dog" width="90%">
</div>


<style>
    .half {
    /* display: flex; */
    float: left;
    width: 50%;
    background-color: rgb(255, 255, 255);
    height: 1000px;
    }

    button {
        width: 90%;
        background: none;
        color: white;
        border: none;
        padding: 0;
        font: inherit;
        cursor: pointer;
        outline: inherit;
        background-color: black;
        margin-top: 20px;
        height: 40px;
    }
</style>