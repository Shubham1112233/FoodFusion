# 🍽️ Food Fusion

**Food Fusion** is a modern, feature-rich recipe management application built with Angular 16 and NgRx for state management. It allows users to create, manage, and organize their favorite recipes while maintaining an integrated shopping list for ingredients.

![Angular](https://img.shields.io/badge/Angular-16.0.0-red?style=flat-square&logo=angular)
![NgRx](https://img.shields.io/badge/NgRx-16.0.0-purple?style=flat-square&logo=ngrx)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0.2-blue?style=flat-square&logo=typescript)
![Bootstrap](https://img.shields.io/badge/Bootstrap-3.4.1-purple?style=flat-square&logo=bootstrap)

## ✨ Features

### 🔐 Authentication & Security
- **User Authentication**: Secure login and signup functionality with Firebase Authentication
- **Route Guards**: Protected routes that require authentication
- **Auto-login**: Persistent authentication using local storage
- **Token Management**: Automatic token refresh and expiration handling

### 📖 Recipe Management
- **Create Recipes**: Add new recipes with detailed information
- **Edit Recipes**: Update existing recipes with ease
- **Delete Recipes**: Remove unwanted recipes
- **Recipe Details**: View comprehensive recipe information including:
  - Recipe name and description
  - Recipe image
  - List of ingredients with quantities
  - Step-by-step instructions

### 🛒 Shopping List
- **Add Ingredients**: Quickly add ingredients to your shopping list
- **Edit Items**: Modify ingredient quantities and names
- **Delete Items**: Remove items from the shopping list
- **Recipe Integration**: Add all recipe ingredients to shopping list with one click

### 💾 Data Persistence
- **Firebase Integration**: Store and sync recipes across devices
- **Save Data**: Manually save recipes to Firebase
- **Fetch Data**: Retrieve saved recipes from Firebase
- **Real-time Sync**: Automatic synchronization with the backend

### 🎨 User Interface
- **Responsive Design**: Mobile-friendly interface using Bootstrap 3
- **Modern Styling**: Clean and intuitive user experience
- **Loading Indicators**: Visual feedback during operations
- **Error Handling**: User-friendly error messages and alerts

## 🏗️ Architecture

### State Management (NgRx)
The application uses **NgRx** for centralized state management, providing:
- Predictable state updates
- Time-travel debugging with Redux DevTools
- Side effect management with NgRx Effects
- Type-safe actions and reducers

### Module Structure
```
src/app/
├── auth/                 # Authentication module
│   ├── store/           # Auth state management
│   ├── auth.service.ts  # Authentication service
│   └── auth.guard.ts    # Route guard
├── recipes/             # Recipes module
│   ├── store/          # Recipe state management
│   ├── recipe-list/    # Recipe listing component
│   ├── recipe-detail/  # Recipe detail view
│   └── recipe-edit/    # Recipe form
├── shopping-list/       # Shopping list module
│   ├── store/          # Shopping list state
│   └── shopping-edit/  # Shopping list editor
├── shared/             # Shared components and utilities
│   ├── alert/         # Alert component
│   ├── loading-spinner/ # Loading indicator
│   └── directives/    # Reusable directives
└── store/             # Root state configuration
```

## 🚀 Getting Started

### Prerequisites
- **Node.js** (v14 or higher)
- **npm** (v6 or higher)
- **Angular CLI** (v16)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd FoodFusion-main
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure Firebase**
   - Create a Firebase project at [Firebase Console](https://console.firebase.google.com/)
   - Enable Authentication (Email/Password)
   - Enable Realtime Database
   - Copy your Firebase API key
   - Update `src/environments/environment.ts` with your Firebase API key:
     ```typescript
     export const environment = {
       production: false,
       firebaseAPIKey: 'YOUR_FIREBASE_API_KEY_HERE'
     };
     ```

4. **Run the development server**
   ```bash
   npm start
   ```
   Navigate to `http://localhost:4200/`

5. **Build for production**
   ```bash
   npm run build
   ```
   Build artifacts will be stored in the `dist/` directory.

## 📋 Available Scripts

| Command | Description |
|---------|-------------|
| `npm start` | Start development server on `http://localhost:4200` |
| `npm run build` | Build the project for production |
| `npm run watch` | Build and watch for changes |
| `npm test` | Run unit tests via Karma |

## 🛠️ Technologies Used

### Core Framework
- **Angular 16**: Modern web application framework
- **TypeScript 5.0.2**: Typed superset of JavaScript
- **RxJS 7.8.0**: Reactive programming library

### State Management
- **@ngrx/store**: Reactive state management
- **@ngrx/effects**: Side effect model for NgRx
- **@ngrx/router-store**: Router integration for NgRx
- **@ngrx/store-devtools**: Developer tools for debugging

### UI & Styling
- **Bootstrap 3.4.1**: Responsive CSS framework
- **Custom CSS**: Modern, clean styling with animations

### Backend & Authentication
- **Firebase**: Backend as a Service (BaaS)
  - Authentication
  - Realtime Database
  - Secure API endpoints

## 📖 User Guide

### Creating Your First Recipe

1. **Sign Up / Login**
   - Navigate to the Authentication page
   - Create a new account or log in to an existing one

2. **Add a Recipe**
   - Click on "Recipes" in the navigation bar
   - Click the "New Recipe" button
   - Fill in the recipe details:
     - Name
     - Description
     - Image URL
     - Ingredients (name and quantity)
   - Click "Save" to create the recipe

3. **Managing Recipes**
   - Click on a recipe to view details
   - Use the "Manage Recipe" dropdown to:
     - Add ingredients to shopping list
     - Edit the recipe
     - Delete the recipe

### Using the Shopping List

1. **Add Items Manually**
   - Navigate to "Shopping List"
   - Enter ingredient name and amount
   - Click "Add"

2. **Add from Recipe**
   - View a recipe
   - Click "To Shopping List" in the Manage Recipe menu
   - All ingredients are added automatically

3. **Edit Items**
   - Click on an item in the shopping list
   - Modify the values in the form
   - Click "Update"

### Saving and Fetching Data

- **Save Data**: Click "Manage" → "Save Data" to sync recipes to Firebase
- **Fetch Data**: Click "Manage" → "Fetch Data" to retrieve saved recipes

## 🔒 Security Features

- **HTTP Interceptors**: Automatic token attachment to requests
- **Route Guards**: Prevent unauthorized access
- **Token Expiration**: Automatic logout on token expiration
- **Secure Storage**: Encrypted data storage in Firebase

## 🎯 Future Enhancements

- [ ] Recipe categories and tags
- [ ] Advanced search and filtering
- [ ] Recipe ratings and reviews
- [ ] Meal planning calendar
- [ ] Print recipe functionality
- [ ] Share recipes with other users
- [ ] Import recipes from URLs
- [ ] Nutrition information
- [ ] Grocery store integration
- [ ] Dark mode support

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the MIT License.

## 👨‍💻 Developer

Built with ❤️ using Angular and NgRx

## 🐛 Known Issues

- Ensure your Firebase API key is properly configured
- Bootstrap 3 CDN must be accessible for proper styling
- Image URLs must be valid and accessible

## 📞 Support

For issues, questions, or suggestions, please create an issue in the repository.

---

**Happy Cooking! 🍳**
