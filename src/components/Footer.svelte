<script>
	import Footer from './Footer.svelte';

</script>

<footer>

    <div class="navigation">
        <img class="logo" src="src/assets/logo.jpg" alt="logo">
        <h2>
            Маленька <br>мережа <br>кавярень
        </h2>
    </div>

    <div class="adres">
        <h3>Наші<br>локації</h3>
        <a title="Тицяй" href="https://maps.app.goo.gl/7AkDQK1xMxDSZyhz7">Поблизу TЦ<br> Глобус</a>
        <a title="Тицяй" href="https://maps.app.goo.gl/ZQWHCvRYBLmBKDre6">Поблизу ЖД<br> вокзалу</a>
        <a title="Тицяй" href="https://maps.app.goo.gl/9YpEpb7AGoZmB9M67">Поблизу ТРЦ<br> Промінь</a>
        <p title="Скоро нова локація">Наведи</p>
    </div>

    <div class="contect">
        <div class="contact">
            <a class="a" tabindex="4" href="https://www.instagram.com/coffee_mishka/">instagram</a>
            <a class="a" tabindex="2" href="https://www.work.ua/jobs/by-company/1873117/">vacancy</a>
            <a class="a" tabindex="3" href="https://www.facebook.com/coffee.mishka/videos/">Facebook</a>
        </div>
        <h3>Тулефон: <br> +380 (066) 785 55 12</h3>
    </div>

</footer>

<style>
    h2{
        margin-bottom: 15px;
        font-weight: 900;
    }
    h3{
        margin-bottom: 15px;
        font-weight: 900;
    }
    a{
        margin-bottom: 10px;
    }
    .a{
        padding: 10px;
        border-radius: 10px;
        background-color: rgb(127, 127, 80);
        margin-bottom: 20px;
        transition: all 0.4s ease-in-out
       }
    .a:hover{
        background-color: rgb(158, 158, 93);
        scale: 1.1;
    }
    .contact{
        display: flex;
        align-items: center;
        flex-direction: column;
        min-width: 300px;
    }
    .navigation{
        align-items: center;
        display: flex;
        flex-direction: column;
    }
    .adres{
        align-items: center;
        display: flex;
        flex-direction: column;
    }
    .contect{
        align-items: center;
        display: flex;
        flex-direction: column;
    }
    footer{
        padding:25px;
        position: relative;
        width: 100%;
        height: 320px;
        background-color: rgba(113, 113, 72);
        display: flex;
        justify-content: space-around;
    }
    .logo{
        margin-bottom: 20px ;
        width: 70px;
        height: 70px;
        border-radius: 50px;

    }
    @media (max-width: 768px) {
        footer{
            flex-direction: column;
            justify-content: flex-start;
            height: auto;

        }
        a{
            font-size: 30px;
        }
        h2{
            font-size: 30px;
        }
        h3{
            font-size: 30px;
        }
        p{
            font-size: 30px;

        }
        .logo{
            width: 200px;
            height: 200px;
            border-radius: 50%;
        }
    }
</style>