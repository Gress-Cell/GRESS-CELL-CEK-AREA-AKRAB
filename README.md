<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Cek Area XL</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f9f9f9;
    }
    header {
      background-color: #007BFF;
      color: white;
      text-align: center;
      padding: 10px 0;
    }
    .container {
      padding: 20px;
    }
    .card {
      background: white;
      border: 1px solid #ddd;
      border-radius: 5px;
      padding: 15px;
      margin-bottom: 10px;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    }
    .card h2 {
      margin: 0 0 10px 0;
      color: #333;
    }
    .card ul {
      padding-left: 20px;
      margin: 0;
    }
    .card ul li {
      list-style: circle;
      color: #555;
    }
    .card p {
      margin: 10px 0 0 0;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <header>
    <h1>Cek Area XL</h1>
  </header>
  <div class="container" id="area-container">
    <!-- Data akan dimasukkan di sini oleh JavaScript -->
  </div>

  <script>
    // Data area XL
    const data = [
      {
        provinsi: "Banten",
        kota_kabupaten: ["Kota Tangerang Selatan", "Kota Tangerang", "Kab. Tangerang"],
        area: "Area 2"
      },
      {
        provinsi: "DI Yogyakarta",
        kota_kabupaten: ["Kab. Kulon Progo", "Kota Yogyakarta", "Kab. Sleman"],
        area: "Area 1"
      },
      {
        provinsi: "Jawa Barat",
        kota_kabupaten: ["Bandung", "Bekasi", "Depok"],
        area: "Area 3"
      }
    ];

    // Menampilkan data ke dalam HTML
    const container = document.getElementById('area-container');

    data.forEach(item => {
      const card = document.createElement('div');
      card.className = 'card';

      const provinsi = document.createElement('h2');
      provinsi.textContent = item.provinsi;

      const list = document.createElement('ul');
      item.kota_kabupaten.forEach(kota => {
        const listItem = document.createElement('li');
        listItem.textContent = kota;
        list.appendChild(listItem);
      });

      const area = document.createElement('p');
      area.textContent = `Area: ${item.area}`;

      card.appendChild(provinsi);
      card.appendChild(list);
      card.appendChild(area);

      container.appendChild(card);
    });
  </script>
</body>
</html>
