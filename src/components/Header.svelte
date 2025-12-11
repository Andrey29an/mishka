<script>
	import Header from './Header.svelte';

</script>

<header>
    <img class="logo" src="src/assets/logo.jpg" alt="logo">

    <div class="contact">
            <a class="a" tabindex="4" href="https://www.instagram.com/coffee_mishka/">instagram</a>
            <a class="a" tabindex="2" href="https://www.work.ua/jobs/by-company/1873117/">vacancy</a>
            <a class="a" tabindex="3" href="https://www.facebook.com/coffee.mishka/videos/">Facebook</a>
    </div>
</header>

<style>
    .logo{
        width: 70px;
        height: 70px;
        border-radius: 50px;

    }
    header{
        box-shadow: 4px 6px 6px  rgb(0, 0, 0);
        height: 110px;
        align-items: center;
        width: 90%;
        display: flex;
        justify-content: space-between;
        background-color: rgba(113, 113, 72);
        margin-top: 20px;
        padding: 0px 45px;
        
    }
    .a{
        padding: 10px;
        border-radius: 10px;
        background-color: rgb(127, 127, 80);
        margin-left: 20px;
        transition: all 0.4s ease-in-out
       }
    .a:hover{
        background-color: rgb(158, 158, 93);
        scale: 1.1;
    }

    .contact{
        display: flex;
        align-items: center;
        justify-content: space-between;
        min-width: 300px;
    }
</style>