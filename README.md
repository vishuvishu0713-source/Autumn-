HTML
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Shoes Store</title>
<style>
    body {
        font-family: Arial;
        margin: 0;
        background: #f5f5f5;
    }
    header {
        background: black;
        color: white;
        padding: 15px;
        text-align: center;
    }
    .container {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }
    .card {
        background: white;
        margin: 15px;
        padding: 15px;
        border-radius: 10px;
        width: 200px;
        text-align: center;
        box-shadow: 0 0 10px rgba(0,0,0,0.2);
    }
    .card img {
        width: 100%;
    }
    button {
        background: black;
        color: white;
        border: none;
        padding: 10px;
        cursor: pointer;
    }
    #cart {
        position: fixed;
        right: 0;
        top: 0;
        background: white;
        width: 250px;
        height: 100%;
        padding: 10px;
        box-shadow: -2px 0 10px rgba(0,0,0,0.3);
    }
</style>
</head>

<body>

<header>
    <h1>👟 Shoes Store</h1>
</header>

<div class="container">
    <div class="card">
        <img src="https://via.placeholder.com/200">
        <h3>Running Shoes</h3>
        <p>₹999</p>
        <button onclick="addToCart('Running Shoes', 999)">Add to Cart</button>
    </div>

    <div class="card">
        <img src="https://via.placeholder.com/200">
        <h3>Casual Shoes</h3>
        <p>₹799</p>
        <button onclick="addToCart('Casual Shoes', 799)">Add to Cart</button>
    </div>

    <div class="card">
        <img src="https://via.placeholder.com/200">
        <h3>Sports Shoes</h3>
        <p>₹1299</p>
        <button onclick="addToCart('Sports Shoes', 1299)">Add to Cart</button>
    </div>
</div>

<div id="cart">
    <h2>🛒 Cart</h2>
    <ul id="cartItems"></ul>
    <h3>Total: ₹<span id="total">0</span></h3>
    <button onclick="checkout()">Checkout</button>
</div>

<script>
let total = 0;

function addToCart(name, price) {
    let li = document.createElement("li");
    li.innerText = name + " - ₹" + price;
    document.getElementById("cartItems").appendChild(li);

    total += price;
    document.getElementById("total").innerText = total;
}

function checkout() {
    alert("Payment Successful! (Demo)");
}
</script>

</body>
</html>
