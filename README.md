# TOKO-DESA-JONGGON-JAYA-
Untuk toko online
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Toko Desa Jonggon Jaya</title>
<style>
 body{font-family:Arial; margin:0; background:#f5f5f5}
 header{background:#2e7d32; color:white; padding:15px; text-align:center; position:sticky; top:0; z-index:10}
 header h2{margin:5px 0}
 .kategori{display:flex; overflow-x:auto; gap:10px; padding:10px; background:white; box-shadow:0 2px 3px #ddd}
 .kat-item{padding:8px 15px; background:#e8f5e9; border-radius:20px; white-space:nowrap; cursor:pointer; border:1px solid #c8e6c9}
 .kat-item.active{background:#2e7d32; color:white}
 .produk{display:grid; grid-template-columns:repeat(2,1fr); gap:10px; padding:10px}
 .card{background:white; border-radius:10px; padding:10px; box-shadow:0 1px 3px #ccc}
 .card img{width:100%; height:120px; object-fit:cover; border-radius:8px}
 .harga{color:#d32f2f; font-weight:bold; font-size:16px}
 .penjual{font-size:12px; color:#555}
 .btn-wa{background:#25D366; color:white; padding:10px; border:none; width:100%; border-radius:5px; margin-top:8px; font-weight:bold}
 .fab{position:fixed; bottom:20px; right:20px; background:#d32f2f; color:white; padding:15px; border-radius:50%; font-size:18px; border:none; box-shadow:0 3px 6px #999}
 .admin-box{background:#fff3cd; padding:10px; margin:10px; border-radius:8px; text-align:center}
</style>
</head>
<body>

<header>
 <h2>🇮🇩 TOKO DESA JONGGON JAYA</h2>
 <p>Jual Beli Hasil Warga 1 Desa</p>
</header>

<div class="admin-box">
 <b>Admin:</b> 0852-4744-7403 <br>
 <small>Hubungi untuk daftar jadi Penjual</small>
</div>

<div class="kategori" id="kategori">
 <div class="kat-item active" onclick="filterKat('Semua')">Semua</div>
 <div class="kat-item" onclick="filterKat('UMKM')">UMKM & Sembako</div>
 <div class="kat-item" onclick="filterKat('Kebun')">Hasil Kebun</div>
 <div class="kat-item" onclick="filterKat('Jasa')">Jasa</div>
 <div class="kat-item" onclick="filterKat('KTK')">Kerajinan KTK</div>
</div>

<div class="produk" id="listProduk">
 <!-- UMKM & SEMBAKO -->
 <div class="card" data-kat="UMKM">
  <img src="https://via.placeholder.com/150/FFC107/000?text=Gorengan">
  <h4>Gorengan Aneka</h4>
  <p class="harga">Rp 1.000 /pcs</p>
  <p class="penjual">Penjual: Warung Gorengan Mama Yono - RT</p>
  <button class="btn-wa" onclick="pesanWA('Gorengan Aneka','Warung Gorengan Mama Yono','085247447403')">Pesan di WA</button>
 </div>
 <div class="card" data-kat="UMKM">
  <img src="https://via.placeholder.com/150/4CAF50/FFF?text=Sembako">
  <h4>Berbagai Sembako</h4>
  <p class="harga">Harga Sesuai Barang</p>
  <p class="penjual">Penjual: Warung Sembako d'tian - RT</p>
  <button class="btn-wa" onclick="pesanWA('Sembako','Warung Sembako d\'tian','085247447403')">Pesan di WA</button>
 </div>
 <div class="card" data-kat="UMKM">
  <img src="https://via.placeholder.com/150/4CAF50/FFF?text=Sembako">
  <h4>Berbagai Sembako</h4>
  <p class="harga">Harga Sesuai Barang</p>
  <p class="penjual">Penjual: Warung Sembako Wasri - RT</p>
  <button class="btn-wa" onclick="pesanWA('Sembako','Warung Sembako Wasri','085247447403')">Pesan di WA</button>
 </div>

 <!-- HASIL KEBUN -->
 <div class="card" data-kat="Kebun">
  <img src="https://via.placeholder.com/150/8BC34A/FFF?text=Singkong">
  <h4>Singkong Segar</h4>
  <p class="harga">Rp 8.000 /kg</p>
  <p class="penjual">Penjual: Pak Sutri - RT</p>
  <button class="btn-wa" onclick="pesanWA('Singkong Segar','Pak Sutri','085247447403')">Pesan di WA</button>
 </div>
 <div class="card" data-kat="Kebun">
  <img src="https://via.placeholder.com/150/FFEB3B/000?text=Pisang">
  <h4>Pisang Kepok</h4>
  <p class="harga">Rp 15.000 /sisir</p>
  <p class="penjual">Penjual: Pak Slamet - RT</p>
  <button class="btn-wa" onclick="pesanWA('Pisang Kepok','Pak Slamet','085247447403')">Pesan di WA</button>
 </div>
 <div class="card" data-kat="Kebun">
  <img src="https://via.placeholder.com/150/CDDC39/000?text=Kacang">
  <h4>Kacang Tanah Kupas</h4>
  <p class="harga">Rp 30.000 /kg</p>
  <p class="penjual">Penjual: Pak Tarban - RT</p>
  <button class="btn-wa" onclick="pesanWA('Kacang Tanah','Pak Tarban','085247447403')">Pesan di WA</button>
 </div>

 <!-- JASA -->
 <div class="card" data-kat="Jasa">
  <img src="https://via.placeholder.com/150/607D8B/FFF?text=Pandai+Besi">
  <h4>Jasa Pandai Besi</h4>
  <p class="harga">Aret, Parang, Dodos, Egrek</p>
  <p class="penjual">Penjual: Sobirin - Produksi Alat Pertanian</p>
  <button class="btn-wa" onclick="pesanWA('Alat Pertanian','Sobirin','085247447403')">Pesan di WA</button>
 </div>
 <div class="card" data-kat="Jasa">
  <img src="https://via.placeholder.com/150/795548/FFF?text=Tukang">
  <h4>Jasa Tukang Bangunan</h4>
  <p class="harga">Rp 150.000 /hari</p>
  <p class="penjual">Penjual: Pak Casmu'i - Tukang Bangunan</p>
  <button class="btn-wa" onclick="pesanWA('Jasa Tukang Bangunan','Pak Casmu\'i','085247447403')">Pesan di WA</button>
 </div>
</div>

<button class="fab" onclick="alert('Hubungi Admin 0852-4744-7403 untuk daftarkan produk/jasa anda secara gratis')">+ JUAL</button>

<script>
function pesanWA(produk, nama, no){
 let text = `Halo ${nama}, saya mau pesan ${produk} dari Toko Desa Jonggon Jaya`;
 window.open(`https://wa.me/62${no.substring(1)}?text=${encodeURIComponent(text)}`);
}

function filterKat(kategori){
 let cards = document.querySelectorAll('.card');
 let btns = document.querySelectorAll('.kat-item');
 btns.forEach(b=>b.classList.remove('active'));
 event.target.classList.add('active');
 
 cards.forEach(card=>{
   if(kategori=='Semua' || card.dataset.kat==kategori){
     card.style.display='block';
   } else {
     card.style.display='none';
   }
 });
}
</script>

</body>
</html>
