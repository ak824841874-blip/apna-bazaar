
<!DOCTYPE html>
<html lang="hi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Apna Bazaar</title>
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f5f6fa;
      color: #222;
    }
    header {
      background: #087f5b;
      color: white;
      padding: 20px 14px;
      text-align: center;
    }
    header h1 { margin: 0 0 8px; }
    .search {
      width: 100%;
      padding: 12px;
      border: 1px solid #ddd;
      border-radius: 8px;
      margin-top: 12px;
      font-size: 16px;
    }
    .banner {
      margin: 16px;
      padding: 24px 16px;
      background: #d3f9d8;
      border-radius: 12px;
      text-align: center;
    }
    .products {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 12px;
      padding: 16px;
    }
    .product {
      background: white;
      border-radius: 10px;
      padding: 14px;
      text-align: center;
      box-shadow: 0 2px 6px #00000012;
    }
    .emoji { font-size: 48px; }
    .price { color: #087f5b; font-weight: bold; }
    button {
      background: #087f5b;
      color: white;
      border: 0;
      border-radius: 7px;
      padding: 10px;
      cursor: pointer;
    }
    footer {
      background: #222;
      color: white;
      text-align: center;
      padding: 18px;
    }
  </style>
</head>
<body>
  <header>
    <h1>🛍️ Apna Bazaar</h1>
    <p>आपकी अपनी ऑनलाइन दुकान</p>
    <input class="search" id="search"
      placeholder="प्रोडक्ट खोजें..."
      oninput="searchProducts()">
  </header>

  <section class="banner">
    <h2>स्वागत है!</h2>
    <p>अपनी पसंद के प्रोडक्ट यहाँ देखें।</p>
  </section>

  <h2 style="padding-left:16px">हमारे प्रोडक्ट</h2>

  <section class="products" id="products">
    <div class="product">
      <div class="emoji">👕</div>
      <h3>टी-शर्ट</h3>
      <p class="price">₹299</p>
      <button onclick="order('टी-शर्ट')">ऑर्डर करें</button>
    </div>
    <div class="product">
      <div class="emoji">👟</div>
      <h3>जूते</h3>
      <p class="price">₹599</p>
      <button onclick="order('जूते')">ऑर्डर करें</button>
    </div>
    <div class="product">
      <div class="emoji">🎒</div>
      <h3>बैग</h3>
      <p class="price">₹399</p>
      <button onclick="order('बैग')">ऑर्डर करें</button>
    </div>
    <div class="product">
      <div class="emoji">⌚</div>
      <h3>घड़ी</h3>
      <p class="price">₹499</p>
      <button onclick="order('घड़ी')">ऑर्डर करें</button>
    </div>
  </section>

  <footer>
    <p>Apna Bazaar © 2026</p>
    <p>आपकी खरीदारी, आपका बाज़ार</p>
  </footer>

  <script>
    function searchProducts() {
      const q = document.getElementById('search')
        .value.toLowerCase();
      document.querySelectorAll('.product').forEach(p => {
        p.style.display =
          p.innerText.toLowerCase().includes(q) ? '' : 'none';
      });
    }

    function order(product) {
      alert('आपने ' + product +
        ' चुना है। ऑर्डर की सुविधा जल्द जोड़ी जाएगी।');
    }
  </script>
</body>
</html>
