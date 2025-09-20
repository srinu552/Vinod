function addToCart(button) {
    const item = button.parentElement;
    const name = item.dataset.name;
    const price = Number(item.dataset.price);
    
    let cart = JSON.parse(localStorage.getItem('cart')) || [];
    cart.push({ name, price });
    localStorage.setItem('cart', JSON.stringify(cart));

    alert(`${name} added to cart!`);
}
