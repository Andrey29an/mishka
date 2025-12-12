
<script >
	import GeleryFoto from './components/GeleryFoto.svelte';
  import "./app.css"
  import Header from "./components/Header.svelte";
  import Footer from './components/Footer.svelte';
  import News from './components/News.svelte';
</script>

<main>
  <Header></Header>
  <h1 class="companyName">
    COFFEE MISHKA
  </h1> 
  <GeleryFoto></GeleryFoto>
  <News></News>
  <Footer></Footer>
</main>
<style>       
main{
  width: 100%;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}
.companyName{
  text-align: center;
  font-size: 150px;
  font-weight: 900;
  font-family:'Gill Sans', 'Gill Sans MT';
}
@media screen and (max-width: 1330px){
  .companyName{
    font-size: 100px;
  }
}
@media screen and (max-width: 850px){
  .companyName{
    margin-top: 40px;
    font-size: 60px;
    line-height: 45px;
  }
}
</style>