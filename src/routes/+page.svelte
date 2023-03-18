<script>
    import {goto, beforeNavigate, afterNavigate} from "$app/navigation";

    const handleClick = () => {
        console.log("Placing Your Order!")
        goto("/products")
    }

    beforeNavigate((navigation) =>{
        console.log({before:navigation})
    })
    afterNavigate((navigation) =>{
        console.log({after:navigation})
    })
</script>



<h1>Welcome to Homepage!</h1>

<a href="/blog">Blog!</a><br>
<a href="/products">Products!</a><br><br>
<button on:click={handleClick}> Place Order! </button>