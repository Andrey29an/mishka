 <script>
    // Дані для галереї
    const photos = [
        { src: "src/assets/завантаження (1).jpeg", alt: "Фото 1" },
        { src: "src/assets/завантаження (2).jpeg", alt: "Фото 2" },
        { src: "src/assets/завантаження (3).jpeg", alt: "Фото 3" },
        { src: "src/assets/завантаження.jpeg", alt: "Фото 4" },
    ];

    // Класи позиціонування (для імітації p1, p2, p3, p4)
    // Ці дані будуть використовуватися для застосування унікальних стилів позиціонування
    const positions = [
        { left: '0%', top: '10%', zIndex: 1 },    // p1: 0, 50px
        { left: '23%', top: '0%', zIndex: 2 },    // p2: 250px, 0
        { left: '46%', top: '10%', zIndex: 3 },   // p3: 500px, 50px
        { left: '69%', top: '0%', zIndex: 4 },    // p4: 750px, 0
    ];
</script>

<div class="gallery-wrapper">
    <div class="gallery-container">
        {#each photos as photo, i}
            <img 
                class="photo" 
                src={photo.src} 
                alt={photo.alt}
                style={`
                    left: ${positions[i].left};
                    top: ${positions[i].top};
                    z-index: ${positions[i].zIndex};
                `}
            />
        {/each}
    </div>
</div>

<style>
    /* ----------------------------------------------------- */
    /* 1. Обгортка та Контейнер */
    /* ----------------------------------------------------- */
    .gallery-wrapper {
        display: flex;
        justify-content: center;
        width: 100%;
        padding: 20px 0;
    }
    
    .gallery-container {
        position: relative;
        /* Адаптивна ширина: 90% від viewport, але не більше 1100px */
        width: 90vw; 
        max-width: 1100px;
        /* Висота контейнера, щоб вмістити всі фото (важливо для absolute) */
        min-height: 500px; 
        margin: 0 auto;
    }

    /* ----------------------------------------------------- */
    /* 2. Стилі Фотографій (на базі відсотків) */
    /* ----------------------------------------------------- */
    .photo {
        /* Ширина: приблизно 320px від 1100px = ~29% */
        width: 29%; 
        /* Висота: приблизно 420px від 500px = 84% */
        height: 84%; 
        max-width: 320px; /* Обмежуємо максимальну ширину */
        max-height: 420px; /* Обмежуємо максимальну висоту */

        object-fit: cover;
        position: absolute;
        border-radius: 30px;
        box-shadow: 0 10px 20px rgba(0, 0, 0, 0.25);
        transition: transform 0.4s ease, z-index 0s 0.4s;
        /* Курсор допомагає зрозуміти, що елемент інтерактивний */
        cursor: pointer; 
    }
    
    .photo:hover {
        transform: scale(1.05);
        z-index: 100; /* Піднімаємо над усіма іншими */
        transition: transform 0.4s ease, z-index 0s;
    }

    /* ----------------------------------------------------- */
    /* 3. Media Query: Мобільний вигляд (перехід до вертикального стека) */
    /* ----------------------------------------------------- */
    @media (max-width: 768px) {
        .gallery-container {
            /* Значно збільшуємо висоту, щоб вмістити елементи вертикально */
            min-height: 1000px; 
            width: 100%;
        }

        .photo {
            width: 100%; /* Фото займає майже всю ширину */
            height: 250px; /* Фіксована висота на мобільному */
            /* max-width: none; */
            
            /* Переписуємо позиціонування для вертикального стека */
            left: 50% !important; /* Центруємо горизонтально */
            transform: translateX(-50%);
            z-index: 10; /* Піднімаємо всі фото над фоном */
        }
        
        /* Вертикальне позиціонування (динамічні стилі перекриваються) */
        /* Використовуємо кастомні класи, щоб було простіше, якщо потрібно: */
        .photo:nth-child(1) { top: 0px !important; }
        .photo:nth-child(2) { top: 260px !important; }
        .photo:nth-child(3) { top: 520px !important; }
        .photo:nth-child(4) { top: 780px !important; }
        
        .photo:hover {
            /* Трохи менше збільшення, щоб не виходило за межі екрана */
            transform: scale(1.03) translateX(-50%); 
        }
    }
</style>