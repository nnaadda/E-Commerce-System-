# 🛒 Java Console E-Commerce System

This is a **Java-based console application**.

The system simulates a simple e-commerce experience, including product management, a shopping cart, shipping logic, and checkout functionality.

---

## 🎯 Project Purpose

The goal is to design and implement an e-commerce system that satisfies the challenge requirements:

> ✅ Define products (name, price, quantity, expiry, shipping info)  
> ✅ Allow customers to add products to a cart  
> ✅ Handle expired or unavailable products  
> ✅ Implement checkout with subtotal, shipping, and total  
> ✅ Collect and ship applicable products  
> ✅ Follow clean code and OOP best practices

---

## 🧩 Features

### 📦 Product Management
- Products have:
  - `name`, `price`, `quantity`
  - Optional expiry date
  - Optional shipping flag + weight
- Distinguishes between:
  - Expirable vs Non-expirable
  - Shippable vs Non-shippable

### 🛒 Cart Operations
- Add products by name and quantity
- Checks:
  - Product exists
  - Product is not expired
  - Enough stock is available
- Maintains list of cart items

### ✅ Checkout Process
- Validates:
  - Cart not empty
  - No expired items
  - Sufficient balance
- Calculates:
  - Subtotal (item prices)
  - Shipping cost (shippable weight × 12)
  - Total amount and updates balance

### 🚚 Shipping Service
- Gathers all shippable items
- Uses a simple `ShippableItem` interface
- Prints:
  - Each shipped item with weight
  - Total package weight

---

## 🧪 Example Run

```java
Cart cart = new Cart(productList);
cart.addToCart("Cheese", 2);
cart.addToCart("TV", 1);
cart.addToCart("Scratch Card", 1);

Customer customer = new Customer(10000.0, cart);
customer.checkout();


Here's how you can include the output in your `README.md` file under an **Example Output** section:

---

```markdown
## 🧾 Example Console Output

```

Added 2 x Cheese
Cannot add Biscuits: product is expired.
Cannot add TV: product is expired.
Cannot add Scratch Card: product is expired.
Cannot add Milk: product is expired.
Product Camera not found.

Cart Items:

* Cheese x 2

\*\* Shipment notice \*\*
Item               Weight
-------------------------

* Cheese | Weight: 2.0kg
* Cheese | Weight: 2.0kg
  Total package weight: 4.0kg

\*\* Checkout receipt \*\*
2x Cheese       200.0
---------------------

Subtotal         200.0
Shipping         24.0
Amount           224.0
Balance Left     11776.0
END.

```

---

```
