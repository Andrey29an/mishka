<script>

</script>

<div class="gallery-container">
    <img class="photo p1 "src="src/assets/завантаження (1).jpeg" alt="">
    <img class="photo p2 "src="src/assets/завантаження (2).jpeg" alt="">
    <img class="photo p3 "src="src/assets/завантаження (3).jpeg" alt="">
    <img class="photo p4" src="src/assets/завантаження.jpeg" alt="">
</div>
    

<style>
    .gallery-container {
            position: relative;
            width: 1100px; 
            height: 500px;
        }

        .photo {
            width: 320px;
            height: 420px;
            object-fit: cover;
            position: absolute;
            border-radius: 30px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.25);
            transition: transform 0.4s ease;
        }
        

        .photo:hover {
            transform: scale(1.05);
            z-index: 100 !important;
        }
        .p1 {
            left: 0;
            top: 50px;
            z-index: 1;
        }
        .p2 {
            left: 250px;
            top: 0px;
            z-index: 2;
        }
        .p3 {
            left: 500px;
            top: 50px; 
            z-index: 3;
        }
        .p4 {
            left: 750px;
            top: 0px;   
            z-index: 4;
        }
</style>