

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
    <img src={src}>

    
</div>