# 👟 Step-Smart — Footwear Shopping Platform

Step-Smart is a modern **web-based footwear shopping platform** designed to provide users with a convenient and interactive way to browse footwear products, explore different categories, view product details, manage their shopping cart, and proceed toward checkout.

The application is built with **React and Vite** and uses reusable components to create different parts of the shopping experience. Product information is retrieved dynamically and displayed through an organized product catalogue with sorting, category options, pagination, and product cards.

---

## 🚀 Features

* 👟 Browse a wide range of footwear products
* 🛍️ Product catalogue with organized product cards
* 👠 Women's footwear category
* 🔎 Product browsing and category navigation
* 💰 Price-based sorting
* 📄 Pagination for product listings
* 🖼️ Product images and product information
* 📋 Individual product details
* 🛒 Add products to shopping cart
* 🗑️ Remove products from cart
* 🔐 Login functionality
* 👤 Authentication state management
* 💳 Checkout and payment interface
* 📱 Responsive component-based UI
* 🎨 Modern interface using Chakra UI
* ✨ Interactive UI elements and animations

---

# 🛠️ Technologies Used

| Technology                  | Purpose                              |
| --------------------------- | ------------------------------------ |
| **React.js**                | Building the frontend application    |
| **Vite**                    | Development server and build tool    |
| **JavaScript**              | Application logic                    |
| **Chakra UI**               | UI components and styling            |
| **React Router**            | Navigation between application pages |
| **Axios**                   | HTTP requests and data handling      |
| **JSON Server / JSON data** | Product data management              |
| **Swiper**                  | Product/image slider functionality   |
| **Framer Motion**           | UI animations                        |
| **React Icons**             | Icons used throughout the interface  |
| **CSS**                     | Additional application styling       |

The project's package configuration confirms React, Vite, Chakra UI, Axios, React Router, Swiper, Framer Motion and React Icons as major dependencies.

---

# 📂 Project Structure

```text
Step-Smart/
│
├── public/
│
├── src/
│   ├── assets/
│   │
│   ├── components/
│   │   ├── Addtocart.jsx
│   │   ├── AllRoutes.jsx
│   │   ├── Card.jsx
│   │   ├── Footer.jsx
│   │   ├── Homepage.jsx
│   │   ├── Login.jsx
│   │   ├── Midpage.jsx
│   │   ├── Navbar.jsx
│   │   ├── Pagination.jsx
│   │   ├── Payment.jsx
│   │   ├── Product.jsx
│   │   ├── ProductDetails.jsx
│   │   ├── Sandles.jsx
│   │   ├── SingleProduct.jsx
│   │   └── Swiper.jsx
│   │
│   ├── App.css
│   ├── App.jsx
│   ├── AuthContextProvider.jsx
│   ├── SignUp.jsx
│   ├── index.css
│   └── main.jsx
│
├── db.json
├── index.html
├── package.json
├── package-lock.json
└── vite.config.js
```

The repository currently separates reusable UI components such as the navbar, product catalogue, cart, login, payment, product details and routing into individual React files.

---

# 🔄 System Workflow

```text
                    ┌─────────────────────┐
                    │      User Opens     │
                    │    Step-Smart       │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │      Homepage       │
                    │  Banner + Content   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Browse Products     │
                    │ Categories / Shoes  │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Product Listing    │
                    │ Sort + Pagination   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Product Details    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Add to Cart     │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Shopping Cart    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Payment / Checkout │
                    └─────────────────────┘
```

---

# 🏠 Homepage

The homepage acts as the starting point of the application.

It combines a **slider section** with additional content sections to create the initial shopping experience.

The React implementation loads the slider and middle-page content through reusable components.

```text
Homepage
   │
   ├── Product / Promotional Slider
   │
   └── Main Content Section
```

---

# 👟 Product Catalogue

The product catalogue is one of the main sections of Step-Smart.

Products are retrieved and displayed dynamically, with the interface providing options for browsing and sorting.

The current product implementation retrieves women's footwear data with pagination and displays the products in a grid layout.

### Product Information

Each product can contain information such as:

```text
Product ID
Product Name
Category
Price
Image
Brand
Color
Product Link
```

The project's `db.json` contains structured product information including titles, categories, prices, images, colours and brand information.

---

# 🔍 Product Filtering & Sorting

The product page provides users with different ways to explore the catalogue.

### Categories

Example categories include:

```text
Boat Shoes
Boots
Clogs & Mules
Flats
Heels
Loafers & Oxfords
Slippers
Sneakers
```

### Brand Options

```text
Adidas
Sketchers
Puma
```

### Colour Options

```text
Black
White
Grey
```

The product interface also provides price sorting:

```text
Price: Low → High
Price: High → Low
```

These catalogue controls are implemented within the product browsing component.

---

# 📄 Pagination

To avoid displaying the entire product catalogue on one page, Step-Smart uses pagination.

The application requests products in pages and displays a limited number of products at a time.

```text
Product Dataset
      ↓
Page 1
      ↓
Products
      ↓
Next Page
      ↓
More Products
```

This makes browsing a large collection more manageable.

---

# 🛍️ Product Details

Users can move from the product listing to product-related detail views.

The application uses separate React components for product display, individual products and product details, keeping the interface modular and easier to maintain.

A typical product journey is:

```text
Product Listing
       ↓
Select Product
       ↓
View Product Information
       ↓
Add to Cart
```

---

# 🛒 Shopping Cart

Step-Smart includes a dedicated shopping cart section.

Products stored in the cart are displayed with:

* Product image
* Product name
* Product price
* Quantity controls
* Remove option
* Subtotal area
* Checkout/payment navigation

The cart component maintains product information through the application's authentication/context state and provides a remove-product action.

```text
Selected Product
       ↓
    Add to Cart
       ↓
 Shopping Cart
       ↓
Review Items
       ↓
Remove / Modify
       ↓
Proceed to Checkout
```

---

# 🔐 Login & Authentication

The application includes a login interface for users.

The login component validates the entered credentials and displays feedback messages for:

* Successful login
* Empty required fields
* Invalid credentials

The authentication state is maintained using a custom React Context provider.

### Authentication Flow

```text
User
 ↓
Login Page
 ↓
Enter Email + Password
 ↓
Validate Credentials
 ↓
 ┌───────────────┐
 │               │
 ▼               ▼
Valid          Invalid
 │               │
 ▼               ▼
Login          Error Message
Successful
```

---

# 👤 Authentication Context

Step-Smart uses a custom `AuthContext` to manage authentication-related state.

The context provides:

```text
auth
login()
logout()
data
setData()
```

This allows different components to access and update shared application state without passing the same information through every component manually.

---

# 💳 Payment & Checkout

The application contains a payment page where users can enter checkout information.

The payment interface includes fields for:

```text
First Name
Last Name
Address
Credit Card Number
CVV
```

A confirmation modal is displayed before completing the checkout flow.

### Checkout Flow

```text
Shopping Cart
      ↓
Payment Page
      ↓
Enter Details
      ↓
Proceed
      ↓
Confirmation
      ↓
Order Completion
```

**Note:** The current implementation provides a frontend payment/checkout interface; it should not be presented as a real payment gateway integration.

---

# 🧩 Component-Based Architecture

The application follows a component-based React architecture.

```text
                     App
                      │
          ┌───────────┼───────────┐
          ▼           ▼           ▼
       Navbar       Routes      Footer
                      │
          ┌───────────┼──────────────┐
          ▼           ▼              ▼
      Homepage     Products        Login
                      │
             ┌────────┼────────┐
             ▼        ▼        ▼
          Details    Cart    Payment
```

The main `App.jsx` loads the navigation bar, route configuration and footer around the application content.

---

# 🧭 Application Routes

The project uses **React Router** to handle navigation.

Current routes include:

```text
/                   → Homepage
/login              → Login
/product            → Product Catalogue
/women/:id          → Women's Products
/productDetails     → Product Details
/addtocart          → Shopping Cart
/payment            → Payment
```

These routes are defined in the project's `AllRoutes.jsx` component.

---

# 🗃️ Product Data

The repository contains a `db.json` file with structured footwear product information.

The product records include details such as:

```text
Article Code
Title
Category
Price
Images
Colours
Brand
Product Link
```

For example, the dataset contains footwear categories such as loafers, boots, court shoes, slingbacks and slides.

---

# 🎨 User Interface

Step-Smart uses **Chakra UI** to build reusable interface components such as:

* Buttons
* Forms
* Inputs
* Grids
* Cards
* Accordions
* Modals
* Layout containers
* Navigation elements

The project also uses React Icons, Swiper and Framer Motion to enhance the visual and interactive experience.

---

# 🧰 Technology Architecture

```text
                     STEP-SMART
                         │
                         ▼
                    React + Vite
                         │
          ┌──────────────┼──────────────┐
          ▼              ▼              ▼
      Chakra UI      React Router     Axios
          │              │              │
          ▼              ▼              ▼
      UI Design      Navigation     Data Requests
                         │
                         ▼
                   Product Catalogue
                         │
          ┌──────────────┼──────────────┐
          ▼              ▼              ▼
       Product          Cart          Payment
       Details
```

---

# ▶️ How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/Amala0402/Step-Smart.git
```

### 2. Open the Project

```bash
cd Step-Smart
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Start the Development Server

```bash
npm run dev
```

Vite is configured as the project's development and build tool.

### 5. Run the Product Data Server

The project also defines a script for running JSON Server:

```bash
npm run server
```

This starts the local JSON data server using `db.json`.

---

# 🎯 Project Highlights

* 👟 Developed a complete frontend concept for a footwear shopping platform
* ⚛️ Built using reusable React components
* 🎨 Designed the interface using Chakra UI
* 🧭 Implemented multi-page navigation with React Router
* 🛍️ Created product browsing and product detail flows
* 🔎 Added product categories and price sorting
* 📄 Implemented pagination for product listings
* 🛒 Developed shopping cart functionality
* 🔐 Added login and authentication-state management
* 💳 Created a checkout and payment interface
* 🗃️ Used structured JSON product data
* ✨ Added interactive UI components and visual effects

---

# 🔮 Future Improvements

The project can be extended into a more complete e-commerce platform by adding:

* 🔹 Real payment gateway integration
* 🔹 Secure user authentication
* 🔹 User registration with database persistence
* 🔹 Backend API integration
* 🔹 Persistent shopping carts
* 🔹 Fully functional product search
* 🔹 Advanced filtering by price, brand, size and colour
* 🔹 Wishlist functionality
* 🔹 Product reviews and ratings
* 🔹 Order history
* 🔹 Inventory management
* 🔹 Admin dashboard
* 🔹 Personalized product recommendations
* 🔹 Responsive mobile-first improvements

---

# 📌 Project Summary

**Step-Smart** demonstrates the development of a modern footwear e-commerce interface using React. It brings together product browsing, category navigation, sorting, pagination, authentication, cart management and checkout into a single web application.

The project follows a **component-based architecture**, making different sections such as products, authentication, cart and payment easier to organize and maintain.

The current implementation focuses primarily on the **frontend shopping experience**, while the project structure provides a foundation for extending it into a complete full-stack e-commerce platform.
