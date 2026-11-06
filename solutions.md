HTML
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Product Listing</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header class="site-header">
        <h1>Tech Store Catalog</h1>
        <p>Explore our latest developer gear and accessories. Resize your browser window to test responsive wrapping.</p>
    </header>

    <main class="main-container">
        <section class="product-grid">
            <!-- Product 1 -->
            <div class="product-card">
                <div class="product-image-wrapper">
                    <img src="images/product1.jpg" alt="Mechanical Keyboard" class="product-image">
                </div>
                <div class="product-info">
                    <h3>Mechanical RGB Keyboard</h3>
                    <p class="product-desc">Hot-swappable mechanical switches with customizable RGB backlight.</p>
                    <div class="product-footer">
                        <span class="price">₹4,499</span>
                        <button class="btn">Add to Cart</button>
                    </div>
                </div>
            </div>

            <!-- Product 2 -->
            <div class="product-card">
                <div class="product-image-wrapper">
                    <img src="images/product2.jpg" alt="Wireless Mouse" class="product-image">
                </div>
                <div class="product-info">
                    <h3>Ergonomic Wireless Mouse</h3>
                    <p class="product-desc">Precision optical sensor with ultra-quiet clicks and long battery life.</p>
                    <div class="product-footer">
                        <span class="price">₹1,899</span>
                        <button class="btn">Add to Cart</button>
                    </div>
                </div>
            </div>

            <!-- Product 3 -->
            <div class="product-card">
                <div class="product-image-wrapper">
                    <img src="images/product3.jpg" alt="Ultrawide Monitor" class="product-image">
                </div>
                <div class="product-info">
                    <h3>29" Ultrawide Monitor</h3>
                    <p class="product-desc">IPS display with HDR10 support for seamless multitasking and coding.</p>
                    <div class="product-footer">
                        <span class="price">₹18,999</span>
                        <button class="btn">Add to Cart</button>
                    </div>
                </div>
            </div>

            <!-- Product 4 -->
            <div class="product-card">
                <div class="product-image-wrapper">
                    <img src="images/product4.jpg" alt="USB-C Hub" class="product-image">
                </div>
                <div class="product-info">
                    <h3>7-in-1 USB-C Hub</h3>
                    <p class="product-desc">Features 4K HDMI, Power Delivery, USB ports, and SD card readers.</p>
                    <div class="product-footer">
                        <span class="price">₹2,499</span>
                        <button class="btn">Add to Cart</button>
                    </div>
                </div>
            </div>

            <!-- Product 5 -->
            <div class="product-card">
                <div class="product-image-wrapper">
                    <img src="images/product5.jpg" alt="Noise Cancelling Headphones" class="product-image">
                </div>
                <div class="product-info">
                    <h3>Active Noise Cancelling Headphones</h3>
                    <p class="product-desc">Over-ear wireless headphones with deep bass and 40-hour playback.</p>
                    <div class="product-footer">
                        <span class="price">₹5,999</span>
                        <button class="btn">Add to Cart</button>
                    </div>
                </div>
            </div>

            <!-- Product 6 -->
            <div class="product-card">
                <div class="product-image-wrapper">
                    <img src="images/product6.jpg" alt="Laptop Stand" class="product-image">
                </div>
                <div class="product-info">
                    <h3>Adjustable Aluminum Laptop Stand</h3>
                    <p class="product-desc">Ergonomic foldable stand designed for improved airflow and posture.</p>
                    <div class="product-footer">
                        <span class="price">₹1,299</span>
                        <button class="btn">Add to Cart</button>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <p>&copy; 2026 Atim Akhtar. All rights reserved.</p>
    </footer>
</body>
</html>
CSS
/* style.css */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, sans-serif;
    background-color: #f8fafc;
    color: #334155;
    line-height: 1.6;
}

.site-header {
    background-color: #0f172a;
    color: #ffffff;
    text-align: center;
    padding: 2.5rem 1rem;
}

.site-header h1 {
    font-size: 1.75rem;
    margin-bottom: 0.5rem;
}

.site-header p {
    color: #94a3b8;
    font-size: 1rem;
}

.main-container {
    max-width: 1200px;
    margin: 2rem auto;
    padding: 0 1.5rem;
}

/* Flexbox Responsive Container */
.product-grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 2rem;
}

/* Product Card Flex Properties: flex-grow: 1, flex-shrink: 1, flex-basis: 260px */
.product-card {
    flex: 1 1 260px;
    max-width: 320px;
    background-color: #ffffff;
    border: 1px solid #e2e8f0;
    border-radius: 12px;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.product-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
}

.product-image-wrapper {
    width: 100%;
    height: 180px;
    background-color: #f1f5f9;
}

.product-image {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.product-info {
    padding: 1.25rem;
    display: flex;
    flex-direction: column;
    flex-grow: 1;
    justify-content: space-between;
}

.product-info h3 {
    font-size: 1.1rem;
    color: #0f172a;
    margin-bottom: 0.5rem;
}

.product-desc {
    font-size: 0.875rem;
    color: #64748b;
    margin-bottom: 1.25rem;
}

.product-footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: auto;
}

.price {
    font-size: 1.15rem;
    font-weight: bold;
    color: #0f172a;
}

.btn {
    background-color: #0284c7;
    color: #ffffff;
    border: none;
    border-radius: 6px;
    padding: 0.5rem 1rem;
    font-size: 0.875rem;
    font-weight: bold;
    cursor: pointer;
    transition: background-color 0.2s ease;
}

.btn:hover {
    background-color: #0369a1;
}

footer {
    text-align: center;
    padding: 1.5rem;
    color: #64748b;
    font-size: 0.875rem;
    border-top: 1px solid #e2e8f0;
    margin-top: 3rem;
}