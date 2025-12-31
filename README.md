# 🌱 Green Earth

A modern, responsive plant e-commerce web application where users can browse plants, filter by categories, add them to their cart, and complete their purchase. Built with vanilla JavaScript and styled with Tailwind CSS.

Green Earth is a single-page application (SPA) that allows users to shop for plants online with an intuitive and eco-friendly interface. The app fetches real-time plant data from an external API, displays it in a responsive grid layout, and provides seamless category filtering and shopping cart functionality. With its "Plant a Tree, Grow a Future" mission, the project promotes environmental awareness while delivering a modern e-commerce experience.

## 🚀 Core Features

- ✅ **Browse Plants** - View a collection of plants with images, descriptions, and pricing fetched from a live API
- 🔍 **Category Filtering** - Filter plants by categories dynamically loaded from the API
- 🛒 **Shopping Cart Management** - Add plants to cart, manage quantities, and view real-time totals
- ➕ **Smart Quantity Handling** - Automatic quantity increment for duplicate items
- ❌ **Remove Items** - Easy removal of items from cart
- 💰 **Real-time Price Calculation** - Automatic total price calculation based on quantity
- ⚡ **Loading States** - Visual feedback with animated spinner during data fetching
- 📱 **Fully Responsive** - Works seamlessly on desktop, tablet, and mobile devices
- 🎨 **Modern UI/UX** - Clean three-column layout with interactive components

## 🛠️ Technologies Used

- **HTML5** - Semantic markup
- **CSS3** - Styling and layout
- **JavaScript (ES6+)** - Vanilla JavaScript for all functionality
- **Tailwind CSS** - Utility-first CSS framework
- **DaisyUI** - Component library for Tailwind CSS
- **Font Awesome** - Icon library
- **Google Fonts** - Poppins and Hind Siliguri typefaces

## 📦 Dependencies

This project uses CDN links for all dependencies (no npm install required):

```html
<!-- Tailwind CSS + DaisyUI -->
<link href="https://cdn.jsdelivr.net/npm/daisyui@5" rel="stylesheet" type="text/css" />
<script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>

<!-- Font Awesome -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/7.0.0/css/all.min.css" />

<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@300;400;500;600;700&family=Poppins:wght@100;200;300;400;500;600;700;800;900&display=swap" rel="stylesheet" />
```

## 🏃 How to Run Locally

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, or Edge)
- No Node.js or npm installation required!

### Step-by-Step Guide

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Assignment-6
   ```

2. **Open the project**
   
   **Option 1: Direct File Opening**
   - Simply double-click `index.html` to open it in your default browser

   **Option 2: Using Live Server (Recommended)**
   - If you have VS Code, install the "Live Server" extension
   - Right-click on `index.html` and select "Open with Live Server"

   **Option 3: Using Python**
   ```bash
   python -m http.server 8000
   # Then visit: http://localhost:8000
   ```

   **Option 4: Using Node.js**
   ```bash
   npx http-server
   # Then visit: http://localhost:8080
   ```

3. **Start browsing!**
   - The app will load automatically and fetch plant data from the API
   - Browse plants, filter by categories, and add items to your cart

## 🔗 Live Links & Resources

- **Live Demo**: [View Live Project](https://your-demo-link.com)
- **Repository**: [GitHub Repository](https://github.com/your-username/Assignment-6)
- **API Documentation**: [Programming Hero Plants API](https://openapi.programming-hero.com)

## 📁 Project Structure

```
Assignment-6/
├── index.html          # Main HTML file with navigation, banner, and layout
├── index.js            # JavaScript functionality (cart, API calls, filters)
├── tailwind.config.js  # Tailwind configuration
├── assets/             # Images (hero-leaf1.png, hero-leaf2.png, etc.)
└── README.md           # Project documentation
```

## 🎨 Design Features

- **Color Scheme**: 
  - Primary Green: `#15803d` (navbar, buttons)
  - Accent Yellow: `#facc15` (CTA buttons)
  - Light Green Background: `#f0fdf4`
  - Category Tags: `#DCFCE7` with green text
  
- **Typography**: 
  - Poppins for English text
  - Hind Siliguri for Bengali/Bangla text

- **Layout**:
  - Three-column responsive grid
  - Sticky shopping cart sidebar
  - Mobile-friendly hamburger menu
  - Card-based plant display

## 🔌 API Endpoints

The application integrates with the following APIs:

| Endpoint | URL | Description |
|----------|-----|-------------|
| All Plants | `https://openapi.programming-hero.com/api/plants` | Fetches all available plants |
| Categories | `https://openapi.programming-hero.com/api/categories` | Retrieves plant categories |
| Filter by Category | `https://openapi.programming-hero.com/api/category/{id}` | Fetches plants by category ID |

### Data Structure
Each plant object includes:
- `name`: Plant name
- `image`: Product image URL
- `description`: Brief description of the plant
- `category`: Plant category/type
- `price`: Price in Bangladeshi Taka (৳)

## ⚙️ How It Works

### Application Flow
1. **Initial Load**: 
   - Fetches and displays all plant categories
   - Loads all plants and displays them in a grid
   - Initializes empty shopping cart

2. **Category Filtering**:
   - User clicks on a category
   - App fetches plants for that specific category
   - Display updates to show only filtered plants
   - "All Trees" option resets to show all plants

3. **Shopping Cart**:
   - User clicks "Add to Cart" on a plant
   - If plant already in cart: quantity increments
   - If new plant: creates new cart item with quantity 1
   - Total price auto-calculates based on quantity × price
   - Remove button (✕) deletes items from cart

### Key JavaScript Functions
- `loadAllTrees()`: Fetches and displays all plants
- `loadCategories()`: Loads category list
- `loadByCategories(id)`: Filters plants by category ID
- `addToCart(plant)`: Adds plant to cart or increments quantity
- `updateTotal()`: Calculates and displays total cart price
- `showLoading()` / `hideLoading()`: Manages loading state

## 💻 Usage

### For Users
1. **Browse Plants**: Scroll through the plant collection displayed in the center grid
2. **Filter by Category**: Click on category names in the left sidebar to filter plants
3. **Add to Cart**: Click the "Add to Cart" button on any plant card
4. **Manage Cart**: 
   - View your selections in the right sidebar
   - See quantity and price for each item
   - Remove items using the ✕ button
5. **View Total**: Check the total price at the bottom of the cart
6. **Reset Filter**: Click "All Trees" to view all plants again

### For Developers
```javascript
// The cart object structure
cart = {
  "Plant Name": {
    quantity: Number,
    price: Number,
    element: HTMLElement
  }
}

// Adding custom categories
// Modify the API endpoint or extend loadCategories()

// Customizing plant display
// Edit the displayTrees() function in index.js
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Author

**Sumaiya Khatun**

## Contact
- GitHub: https://github.com/sumaiyakhatun11
- LinkedIn: http://linkedin.com/in/sumaiya-khatun-web/

For questions or feedback, please open an issue in the repository or reach out via email.

---

<div align="center">
  Made with 💚 for the environment
  <br>
  <sub>Plant a Tree, Grow a Future 🌱</sub>
</div>
