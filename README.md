# Royal Spice Restaurant Website

A beautiful, modern, and fully responsive restaurant website built with React, TypeScript, and Tailwind CSS. This frontend-only application showcases a dynamic menu system, featured dishes, special items, and contact information for Royal Spice Restaurant.

## Features

- **Stunning Hero Section**: Eye-catching landing page with a compelling call-to-action
- **Dynamic Menu System**: Interactive menu with category filtering (58+ food items across 11 categories)
- **Featured Dishes**: Showcase of the restaurant's most popular items
- **Food Gallery**: Visual gallery highlighting the restaurant's culinary offerings
- **Today's Specials**: Dedicated section for special menu items
- **Contact Section**: Complete contact information with a functional contact form
- **Smooth Scrolling Navigation**: Seamless navigation between sections
- **Responsive Design**: Fully optimized for mobile, tablet, and desktop devices
- **Modern Animations**: Smooth transitions and hover effects throughout
- **Colorful Design**: Vibrant orange, red, and yellow gradient theme

## Technologies Used

- **React 18**: Modern React with hooks for state management
- **TypeScript**: Type-safe code for better development experience
- **Tailwind CSS**: Utility-first CSS framework for styling
- **Vite**: Fast build tool and development server
- **Lucide React**: Beautiful icon library
- **Pexels**: High-quality food images

## Menu Categories

1. Starters
2. Mains
3. Lunch Specials
4. Specials
5. Veg Curries
6. Non-Veg Curries
7. Rice & Meals
8. Chinese
9. Fast Food
10. Drinks & Beverages
11. Desserts

## Project Structure

```
royal-spice-restaurant/
├── src/
│   ├── components/
│   │   ├── Navbar.tsx
│   │   ├── Hero.tsx
│   │   ├── FeaturedDishes.tsx
│   │   ├── Gallery.tsx
│   │   ├── Menu.tsx
│   │   ├── Specials.tsx
│   │   ├── Contact.tsx
│   │   └── Footer.tsx
│   ├── data/
│   │   └── menuData.ts
│   ├── App.tsx
│   ├── main.tsx
│   └── index.css
├── index.html
├── package.json
├── tailwind.config.js
├── vite.config.ts
└── README.md
```

## How to Run the Project

### Prerequisites

- Node.js (version 16 or higher)
- npm or yarn package manager

### Installation Steps

1. **Clone the repository**
   ```bash
   git clone <your-repository-url>
   cd royal-spice-restaurant
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm run dev
   ```

4. **Open your browser**
   Navigate to the local URL shown by Vite in the terminal (usually `http://localhost:5173`, or another free port)

### Build for Production

To create a production-ready build:

```bash
npm run build
```

The optimized files will be generated in the `dist` folder.

### Preview Production Build

To preview the production build locally:

```bash
npm run preview
```

## Deployment to GitHub Pages

### Option 1: Using GitHub Actions (Recommended)

1. **Create a `.github/workflows/deploy.yml` file**:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - name: Setup Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '18'

      - name: Install dependencies
        run: npm install

      - name: Build
        run: npm run build

      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./dist
```

2. **Enable GitHub Pages**:
   - Go to your repository settings
   - Navigate to "Pages" section
   - Select "gh-pages" branch as the source
   - Save the changes

3. **Push to GitHub**:
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

### Option 2: Manual Deployment

1. **Build the project**:
   ```bash
   npm run build
   ```

2. **Install gh-pages package**:
   ```bash
   npm install --save-dev gh-pages
   ```

3. **Add deployment scripts to package.json**:
   ```json
   "scripts": {
     "predeploy": "npm run build",
     "deploy": "gh-pages -d dist"
   }
   ```

4. **Update vite.config.ts** to set the correct base path:
   ```typescript
   export default defineConfig({
     base: '/repository-name/',
     plugins: [react()],
   });
   ```

5. **Deploy**:
   ```bash
   npm run deploy
   ```

## Customization Guide

### Updating Menu Items

All menu data is stored in `src/data/menuData.ts`. To add, edit, or remove menu items:

```typescript
{
  id: 59,
  name: "Your Dish Name",
  category: "Category Name",
  price: "₹299",
  description: "Your dish description",
  image: "https://your-image-url.com/image.jpg",
  featured: true, // Optional: set to true for featured dishes
  special: true   // Optional: set to true for special dishes
}
```

### Changing Images

Replace the image URLs in `menuData.ts` with your own images. You can use:
- Pexels (free stock photos)
- Unsplash (free stock photos)
- Your own hosted images

### Updating Contact Information

Edit the contact details in `src/components/Contact.tsx`:
- Address
- Phone numbers
- Email addresses
- Opening hours

### Customizing Colors

The color scheme uses Tailwind CSS classes. Main colors:
- Orange: `orange-500`, `orange-600`
- Red: `red-500`, `red-600`
- Yellow: `yellow-400`

Update these in component files to change the color theme.

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Performance

- Optimized images from Pexels CDN
- Lazy loading for images
- Minimized CSS and JavaScript
- Fast page load times with Vite

## License

This project is open source and available under the MIT License.

## Contact

For any questions or suggestions, please contact:
- Email: info@royalspice.com
- Phone: +91 98765 43210

---

Built with ❤️ using React, TypeScript, and Tailwind CSS
