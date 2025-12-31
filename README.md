# Green Earth

A modern, responsive plant e-commerce web application where users can browse plants, filter by categories, add them to their cart, and complete their purchase. Built with vanilla JavaScript and styled with Tailwind CSS.

## Overview

Green Earth is a single-page application (SPA) that fetches plant data from an external API and displays it in an intuitive, user-friendly interface. The application emphasizes environmental awareness with its "Plant a Tree, Grow a Future" mission.

## Features

### Core Functionality
- **Browse Plants**: View a collection of plants with images, descriptions, and pricing fetched from a live API
- **Category Filtering**: Filter plants by categories dynamically loaded from the API
- **Add to Cart**: Add plants to your shopping cart with a single click
- **Shopping Cart Management**: 
  - View all selected items with quantity tracking
  - Automatic quantity increment for duplicate items
  - Remove items from cart
  - Real-time total price calculation
- **Loading States**: Visual feedback with animated spinner during data fetching
- **Responsive Design**: Fully responsive layout that works on desktop and mobile devices
- **Modern UI**: Built with Tailwind CSS and DaisyUI for a clean, modern interface

### User Interface
- Clean three-column layout: Categories, Plants Grid, Shopping Cart
- Interactive category selector with visual feedback
- Plant cards with images, descriptions, categories, and prices
- Fixed shopping cart sidebar for easy access
- Hero banner with environmental messaging

## Technologies Used

- **HTML5**: Semantic markup
- **JavaScript**: Vanilla JS for dynamic functionality
- **Tailwind CSS**: Utility-first CSS framework
- **DaisyUI**: Component library for Tailwind CSS
- **Font Awesome**: Icon library
- **Google Fonts**: Poppins and Hind Siliguri fonts

## Getting Started

### Prerequisites

A modern web browser (Chrome, Firefox, Safari, or Edge)

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```

2. Navigate to the project directory:
   ```bash
   cd Assignment-6
   ```

3. Open `index.html` in your web browser, or use a local development server:
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js (http-server)
   npx http-server
   ```

4. Visit `http://localhost:8000` in your browser

## Project Structure

```
Assignment-6/
├── index.html          # Main HTML file with navigation, banner, and layout
├── index.js            # JavaScript functionality (cart, API calls, filters)
├── tailwind.config.js  # Tailwind configuration
├── assets/             # Images (hero-leaf1.png, hero-leaf2.png, etc.)
└── README.md           # Project documentation
```

## Design Features

- **Color Scheme**: 
  - Primary Green: `#15803d` (navbar, buttons)
  - Accent Yellow: `#facc15` (CTA buttons)
  - Light Green Background: `#f0fdf4`
  - Category Tags: `#DCFCE7` with green text
  
- **Typography**: 
  - Poppins for English text
  - Hind Siliguri for Bengali/Bangla text

- **Components**:
  - Responsive navbar with mobile menu
  - Hero banner with decorative leaf images
  - Card-based plant display
  - Sticky shopping cart sidebar
  - Loading spinner with green theme

## API

The application integrates with the following APIs:
- **Plants Endpoint**: `https://openapi.programming-hero.com/api/plants` - Fetches all available plants
- **Categories Endpoint**: `https://openapi.programming-hero.com/api/categories` - Retrieves plant categories
- **Category Filter Endpoint**: `https://openapi.programming-hero.com/api/category/{id}` - Fetches plants by specific category

### Data Structure
Each plant object includes:
- `name`: Plant name
- `image`: Product image URL
- `description`: Brief description of the plant
- `category`: Plant category/type
- `price`: Price in Bangladeshi Taka (৳)

## How It Works

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

## Usage

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

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).

## Contact

For questions or feedback, please open an issue in the repository.
