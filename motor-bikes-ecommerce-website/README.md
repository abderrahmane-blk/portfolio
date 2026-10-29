# Motor Bikes — e-commerce website

> a full online shop for a mechanical parts and motorcycle seller , built for a real client with **Django** and **React** .

**Heads up , honest status:** i built this for a client i know in person . when it was deployed for the last round (testing , final touches , showing him the full work) i called him , and he had closed his business and moved to a government job . so it never went live with real customers . everything you see below is the finished app running with mock data .

`Django` · `React` · `REST API` · `Resend (emails)` · `Render` · `Netlify`

---

## What it does

A visitor opens the shop and can browse , search , add to cart and order . no account is forced on him :

- **Logged in** : the cart is saved , and he can see all his previous orders
- **Anonymous** : he can still buy , but the cart is not saved and he can't see old orders
- **Arabic and English** , with the layout flipping to right-to-left for Arabic
- **Product pages** with details and pictures , a product list , and a cart that opens as a side panel
- **Checkout** in clear steps , then an order confirmation page , and a confirmation **email** sent through Resend
- **Contact page** for questions
- **Admin side** : the owner manages the orders and opens any order to see its details
- **Responsive** : works on desktop , tablet and phone (the screenshots are real captures of each size)
- **Full control**: Complete control CRUD operations over Products and Categories for the admin.
- __3 languages__ : Arabic , French , English


## How it's deployed

| part | where |
|---|---|
| React frontend | **Netlify** |
| Django backend + database | **Render** |
| Transactional emails | **Resend** (third-party service) |

The frontend talks to the backend only through the API , so each part can be updated alone.

---

## Screenshots

*Click any image to see it bigger. The long full-page captures are at the end.*

### The main screen

<p align="center">
  <img src="assets/main_view.png" alt="Main screen of the shop" width="90%">
</p>
### Browsing the products

<table>
  <tr>
    <td align="center" width="33%"><img src="assets/Products-page-with-item-in-cart.png" alt="Products page with an item in the cart" width="100%"><br><sub>products , with an item in the cart</sub></td>
    <td align="center" width="33%"><img src="assets/aProductDetails-page.png" alt="Product details page" width="100%"><br><sub>a product's details</sub></td>
    <td align="center" width="33%"><img src="assets/products-list-tiles-ipad.png" alt="Product tiles on iPad" width="100%"><br><sub>product tiles , tablet view</sub></td>
  </tr>
</table>

### Cart

<table>
  <tr>
    <td align="center" width="50%"><img src="assets/cart-page.png" alt="Cart page" width="100%"><br><sub>the cart page</sub></td>
    <td align="center" width="50%"><img src="assets/sideBarCart-ipad.png" alt="Side cart on iPad" width="100%"><br><sub>the side cart (tablet)</sub></td>
  </tr>
</table>

### Checkout

three parts , left to right :

<table>
  <tr>
    <td align="center" width="33%" valign="top"><img src="assets/checkout-page-fullpage-with-mock-data.png" alt="Checkout part 1 with mock data" width="100%"><br><sub>part 1 (with mock data)</sub></td>
    <td align="center" width="33%" valign="top"><img src="assets/checkout-page-part2.png" alt="Checkout part 2" width="100%"><br><sub>part 2</sub></td>
    <td align="center" width="33%" valign="top"><img src="assets/checkout-page-part3.png" alt="Checkout part 3" width="100%"><br><sub>part 3</sub></td>
  </tr>
</table>

### Orders , for the customer and for the owner

<table>
  <tr>
    <td align="center" width="33%"><img src="assets/myOrders-page.png" alt="My orders page" width="100%"><br><sub>customer : my orders</sub></td>
    <td align="center" width="33%"><img src="assets/manageOrders-page2.png" alt="Manage orders page" width="100%"><br><sub>owner : manage orders</sub></td>
    <td align="center" width="33%"><img src="assets/manageOrders-page-an-order-details.png" alt="An order's details" width="100%"><br><sub>owner : one order's details</sub></td>
  </tr>
</table>

---

## Design notes

- **Anonymous checkout on purpose** : forcing an account loses customers , so the account only adds comfort (saved cart , order history) , its not a wall .
- **Separate frontend and backend** : React on Netlify , Django on Render , connected by an API . the frontend can change without touching the server .
- **Emails are not sent from the app itself** : Resend handles delivery , so order emails dont end up in spam as often .
- **Same pages in two languages** , including right-to-left , not a translated copy of the site .

## What it is and what it is not

- built for one real client , tested with mock data , **never used by real customers**
- no live demo link , the business closed before launch
- the source code is not in this repo , i am happy to walk through it on a call

← [back to the portfolio](../README.md)

---

## Full-page screenshots

the whole pages from top to bottom , so they are long . click one to open it full size .

### Desktop

<table>
  <tr>
    <td align="center" width="25%" valign="top"><a href="assets/main-page-fullpage-EN.png"><img src="assets/main-page-fullpage-EN.png" width="100%" alt="Main page English"></a><br><sub>main page , English</sub></td>
    <td align="center" width="25%" valign="top"><a href="assets/main-page-fullpage-AR.png"><img src="assets/main-page-fullpage-AR.png" width="100%" alt="Main page Arabic"></a><br><sub>main page , بالعربية</sub></td>
    <td align="center" width="25%" valign="top"><a href="assets/order-confirmed-page-fullpage.png"><img src="assets/order-confirmed-page-fullpage.png" width="100%" alt="Order confirmed page"></a><br><sub>order confirmed</sub></td>
    <td align="center" width="25%" valign="top"><a href="assets/contact-page-full.png"><img src="assets/contact-page-full.png" width="100%" alt="Contact page"></a><br><sub>contact</sub></td>
  </tr>
</table>

### Tablet and phone

<table>
  <tr>
    <td align="center" width="25%" valign="top"><a href="assets/main-page-fullpage-ipad-AR.png"><img src="assets/main-page-fullpage-ipad-AR.png" width="100%" alt="Main page on iPad in Arabic"></a><br><sub>main page , tablet , بالعربية</sub></td>
    <td align="center" width="25%" valign="top"><a href="assets/products-list-fullpage-ipad.png"><img src="assets/products-list-fullpage-ipad.png" width="100%" alt="Products list on iPad"></a><br><sub>products list , tablet</sub></td>
    <td align="center" width="25%" valign="top"><a href="assets/main_page_fullpage_phone.png"><img src="assets/main_page_fullpage_phone.png" width="100%" alt="Main page on phone"></a><br><sub>main page , phone</sub></td>
    <td align="center" width="25%" valign="top"><a href="assets/product-page-fullpage-iphone.png"><img src="assets/product-page-fullpage-iphone.png" width="100%" alt="Product page on iPhone"></a><br><sub>product page , phone</sub></td>
  </tr>
</table>
