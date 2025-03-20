# 📚 BookVault - Modern E-Library Application

A modern, feature-rich e-library application built with React, TypeScript, and Vite. BookVault provides a seamless reading experience with features like book management, user authentication, and personalized reading lists.

## 🚀 Features

- 📱 Responsive modern UI built with Tailwind CSS and ShadCN
- 🔐 User authentication and authorization
- 📚 Comprehensive book management system
- ⭐ Personalized reading lists and favorites
- 💬 Book reviews and ratings
- 👤 User profiles and reading history
- 🎨 Modern and intuitive interface

## 🛠️ Tech Stack

- **Frontend Framework:** React 18 with TypeScript
- **Build Tool:** Vite
- **Styling:** Tailwind CSS + ShadCN UI
- **State Management:** Zustand
- **Type Safety:** TypeScript
- **Routing:** React Router v6
- **API Client:** Axios
- **Form Handling:** React Hook Form
- **Validation:** Zod
- **Animations:** Framer Motion
- **UI Components:**
  - Headless UI (@headlessui/react)
  - Hero Icons (@heroicons/react)
  - Lucide React (Modern icons)
- **CSS Framework:** Tailwind CSS with PostCSS and Autoprefixer
- **Data Fetching & Caching:** TanStack Query (React Query)
  - Automatic background refetching
  - Cache invalidation
  - Optimistic updates
  - Infinite queries
  - DevTools for debugging
- **Form Validation:** Zod with React Hook Form
- **UI Utilities:**
  - clsx (Conditional class names)
  - tailwind-merge (Tailwind class merging)
  - class-variance-authority (Component variants)
  - tailwindcss-animate (Animation utilities)
- **Notifications:** React Hot Toast

## 🎨 UI/UX Features

- Smooth animations and transitions using Framer Motion
- Accessible UI components with Headless UI
- Beautiful icons from Hero Icons and Lucide React
- Responsive design with Tailwind CSS
- Modern and intuitive user interface
- Toast notifications for user feedback
- Efficient data fetching with React Query
- Form validation with Zod
- Dynamic class name management
- Component variants with class-variance-authority

## 🔧 Data Management

### TanStack Query Setup

The application uses TanStack Query for efficient data fetching and caching. The setup includes:

```typescript
// QueryClient configuration
const queryClient = new QueryClient({
  defaultOptions: {
    queries: {
      staleTime: 60 * 1000, // Data considered fresh for 1 minute
      refetchOnWindowFocus: false, // Disable refetch on window focus
      retry: 1, // Retry failed requests once
    },
  },
});
```

### Example Usage

```typescript
// Fetching data
const { data, isLoading } = useQuery({
  queryKey: ["books"],
  queryFn: () => fetch("/api/books").then((res) => res.json()),
});

// Mutating data
const mutation = useMutation({
  mutationFn: (newBook) => {
    return fetch("/api/books", {
      method: "POST",
      body: JSON.stringify(newBook),
    });
  },
});
```

## 📁 Project Structure

```
e-library/
├── public/
├── src/
│   ├── assets/                  # Static assets
│   ├── components/              # Reusable UI components
│   ├── features/               # Feature-based modules
│   │   ├── auth/              # Authentication
│   │   ├── books/             # Book management
│   │   ├── users/             # User profiles
│   │   └── reviews/           # Reviews system
│   ├── hooks/                 # Custom React hooks
│   ├── layouts/               # Page layouts
│   ├── lib/                   # Utilities and helpers
│   ├── pages/                 # Route pages
│   ├── providers/             # Context providers
│   ├── store/                 # Zustand store
│   ├── styles/                # Global styles
│   └── types/                 # TypeScript types
```

## 🚀 Getting Started

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/bookvault.git
   cd bookvault
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Set up environment variables**

   ```bash
   cp .env.example .env
   ```

   Fill in your environment variables in the `.env` file

4. **Start the development server**

   ```bash
   npm run dev
   ```

5. **Build for production**
   ```bash
   npm run build
   ```

## 🧪 Testing

```bash
# Run unit tests
npm run test

# Run e2e tests
npm run test:e2e
```

## 📝 Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint
- `npm run type-check` - Run TypeScript type checking

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

- Your Name - Initial work - [YourGitHub](https://github.com/yourusername)

## 🙏 Acknowledgments

- ShadCN UI for the beautiful components
- Tailwind CSS for the utility-first CSS framework
- The React community for the amazing ecosystem
