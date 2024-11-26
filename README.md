<html lang="id">
<head>
    <link rel="stylesheet" href="ajak.css">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ajakan Jalan-Jalan BYBY</title>
</head>
<style>
  body {
    font-family: monospace;
    background-image: url(https://wallpaperaccess.com/full/3353813.jpg);
    background-position: top;
    background-size: 1500px;
    background-color: #ffe4e1; /* Warna latar belakang lembut */
    text-align: center;
    font-size: x-large;
    padding: 20px;
    overflow: auto; /* Memungkinkan scroll */
    position: relative; /* Agar elemen anak dapat diposisikan relatif */
}
.hidden {
    display: none;
}
button {
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    padding: 10px 20px;
    margin: 10px;
    background-color: rgba(255, 105, 180, 0.7); /* Warna latar belakang dengan transparansi */
    color: rgb(255, 255, 255);
    border: none;
    border-radius: 1000px;
    cursor: pointer;
    position: relative;
    overflow: hidden; /* Mencegah isi tombol melampaui batas */
}
button:hover {
    background-color: rgba(255, 20, 147, 0.8); /* Warna tombol saat hover */
}

/* Gaya untuk gambar wisata */
#wisata-image {
    display: block; /* Mengatur gambar sebagai block element */
    margin: 20px auto; /* Menempatkan gambar di tengah */
    max-width: 80%; /* Mengatur lebar maksimum gambar */
    height: auto; /* Menjaga rasio aspek gambar */
}

/* Gaya untuk elemen audio */
.audio-container {
    margin-top: 20px; /* Memberikan jarak di atas elemen audio */
    background-color: purple; /* Mengatur warna latar belakang menjadi ungu */
    padding: 10px; /* Memberikan padding di sekitar elemen audio */
    border-radius: 5px; /* Sudut melengkung untuk kontainer audio */
    display: inline-block; /* Agar lebar kontainer sesuai dengan konten */
}

iframe {
    width: 60%; /* Mengatur lebar iframe */
    height: 90px; /* Tinggi iframe, sesuaikan jika diperlukan */
    border: none; /* Menghilangkan border */
}
.flower {
    position: fixed; /* Menggunakan fixed agar tidak mempengaruhi layout */
    width: 50px; /* Ukuran bunga */
    animation: fall 5s linear forwards; /* Animasi jatuh */
    pointer-events: none; /* Membuat bunga tidak menghalangi interaksi */
}

@keyframes fall {
    0% {
        top: -10%;
        opacity: 1;
    }
    100% {
        top: 100%;
        opacity: 0;
    }
}
</style>
<body>

    <h1>JALAN JALAN YUKK BYYBYY!</h1>
    <p>Pilih tempat wisata yang BYBY MAU:</p>

    <div id="menu">
        <button onclick="showWisata('pantai')">Pantai</button>
        <button onclick="showWisata('puncak')">Puncak</button>
        <button onclick="showWisata('kota')">Kota</button>
    </div>

    <div id="wisata" class="hidden">
        <h2 id="wisata-title"></h2>
        <p id="wisata-description"></p>
        <img id="wisata-image" class="hidden" alt="Gambar Wisata">
        <button onclick="backToMenu()">Kembali ke Menu</button>
    </div>

    <div class="audio-container">
        <iframe width="60%" height="90" scrolling="no" frameborder="no" allow="autoplay" 
                src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/1893888144&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true">
        </iframe>
        <div style="font-size: 10px; color: #e018ff; line-break: anywhere; word-break: normal; overflow: hidden; white-space: nowrap; text-overflow: ellipsis; font-family: Interstate, Lucida Grande, Lucida Sans Unicode, Lucida Sans, Garuda, Verdana, Tahoma, sans-serif; font-weight: 50;">
            <a href="https://soundcloud.com/quique-montes-848655910" title="Quique Montes" target="_blank" style="color: #b811ff; text-decoration: none;">Quique Montes</a> · 
            <a href="https://soundcloud.com/quique-montes-848655910/elliot-james-reay-i-think-they" title="Elliot James Reay - I Think They Call This Love" target="_blank" style="color: #ff8fff; text-decoration: none;">Elliot James Reay - I Think They Call This Love</a>
        </div>
    </div>

    <script>
        function showWisata(type) {
            const wisata = document.getElementById('wisata');
            const title = document.getElementById('wisata-title');
            const description = document.getElementById('wisata-description');
            const image = document.getElementById('wisata-image');

            if (type === 'pantai') {
                title.innerText = 'Pantai Sawarna';
                description.innerText = 'AYOOO KE PANTAI SAWARNA BERSAMA BYBY!!!';
                image.src = 'https://th.bing.com/th/id/R.f6d8d3bb8f36e6aefb6490f3a4d8490f?rik=frPlYosOsOZLAQ&riu=http%3a%2f%2f1.bp.blogspot.com%2f-GdbocnKk7fI%2fUjXUX5FHOJI%2fAAAAAAAAAAo%2fGBxgwwr3-EQ%2fs1600%2fgugugugu.jpg&ehk=nRwTpvoIk74%2bHnd1oFzWN%2fmwhtTBQytH5DYmysp41EE%3d&risl=&pid=ImgRaw&r=0'; // Ganti dengan URL gambar pantai
            } else if (type === 'puncak') {
                title.innerText = 'Little Sindbad';
                description.innerText = 'MARI KE LITTLE SINDBAD BYBY!!!';
                image.src = 'https://th.bing.com/th/id/OIP.52qlJO5nOrIXI_kM6V3f4AAAAA?rs=1&pid=ImgDetMain'; // Ganti dengan URL gambar gunung
            } else if (type === 'kota') {
                title.innerText = 'Kota Bandung';
                description.innerText = 'GASKEUN BANDUNG KE -2 KALINYA';
                image.src = 'https://th.bing.com/th/id/OIP.dz4RwLNs527XLM-m6FufzAAAAA?rs=1&pid=ImgDetMain'; // Ganti dengan URL gambar kota
            }

            image.classList.remove('hidden');
            wisata.classList.remove('hidden');
        }

        function backToMenu() {
            const wisata = document.getElementById('wisata');
            const image = document.getElementById('wisata-image');
            image.classList.add('hidden');
            wisata.classList.add('hidden');
        }
        const flowersCount = 10; // Jumlah bunga yang akan ditampilkan
        const flowerTypes = ['🌸', '🌼', '🌺']; // Jenis bunga

    function createFlower() {
        const flower = document.createElement('div');
        flower.className = 'flower';
        flower.innerText = flowerTypes[Math.floor(Math.random() * flowerTypes.length)];
        flower.style.left = Math.random() * 100 + 'vw'; // Posisi acak di sumbu X
        document.body.appendChild(flower);

        // Hapus bunga setelah jatuh
        setTimeout(() => {
            flower.remove();
        }, 6000); // Hapus setelah 5 detik
    }

    // Buat bunga setiap 500ms
    setInterval(createFlower, 200);
    </script>
</body>
</html>
