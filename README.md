# Tata - React Native App

A modern React Native application built with Expo, featuring TypeScript, NativeWind, App Router, and Supabase integration.

## 🚀 Tech Stack

- **React Native** with Expo SDK 53
- **TypeScript** for type safety
- **NativeWind** for styling with Tailwind CSS
- **Expo Router** for file-based navigation (App Router)
- **Supabase** for backend services and authentication

## 📦 Features

- File-based routing with Expo Router
- TypeScript support with strict mode
- Utility-first styling with NativeWind (Tailwind CSS)
- Supabase integration for backend services
- Pre-configured ESLint and Prettier
- Path aliases (`@/*`) for cleaner imports

## 🛠️ Getting Started

### Prerequisites

- Node.js 18+ 
- npm or yarn
- Expo CLI
- iOS Simulator / Android Emulator or physical device

### Installation

1. Clone the repository:
```bash
git clone https://github.com/lewisdonovan/tata.git
cd tata
```

2. Install dependencies:
```bash
npm install
```

3. Set up Supabase:
   - Go to [database.new](https://database.new) to create a new Supabase project
   - Get your Project URL and anon key from the API settings
   - Copy the `.env` file and add your Supabase credentials:
   ```
   EXPO_PUBLIC_SUPABASE_URL=your_supabase_url
   EXPO_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
   ```

4. Start the development server:
```bash
npm start
```

### Available Scripts

- `npm start` - Start the Expo development server
- `npm run ios` - Start on iOS simulator
- `npm run android` - Start on Android emulator  
- `npm run web` - Start web version
- `npm run lint` - Run ESLint and Prettier checks
- `npm run format` - Fix ESLint issues and format code

## 📁 Project Structure

```
├── app/                # App Router pages
│   ├── _layout.tsx     # Root layout
│   ├── index.tsx       # Home page
│   └── details.tsx     # Details page
├── components/         # Reusable components
├── utils/             # Utility functions
│   └── supabase.ts    # Supabase client configuration
├── assets/            # Static assets
└── global.css         # Global styles
```

## 🎨 Styling

This project uses NativeWind, which brings Tailwind CSS to React Native. You can use familiar Tailwind classes in your components:

```tsx
<View className="flex-1 items-center justify-center bg-white">
  <Text className="text-xl font-bold text-blue-600">Hello World!</Text>
</View>
```

## 🔗 Navigation

The app uses Expo Router for file-based navigation. Create new pages by adding files to the `app/` directory:

- `app/index.tsx` → `/` (Home)
- `app/details.tsx` → `/details`
- `app/profile/index.tsx` → `/profile`

## 🔐 Authentication

Supabase is pre-configured for authentication. The client is available in `utils/supabase.ts` and includes:

- AsyncStorage for session persistence
- Auto token refresh
- Cross-platform support

## 📱 Development

The project includes:

- TypeScript with strict mode
- ESLint with Expo config
- Prettier for code formatting
- Path aliases for cleaner imports
- Hot reloading for fast development

## 🚀 Deployment

To deploy your app:

1. For Expo Application Services (EAS):
```bash
npx eas build
```

2. For app stores, follow the [Expo deployment guide](https://docs.expo.dev/distribution/introduction/)

## 📚 Learn More

- [Expo Documentation](https://docs.expo.dev/)
- [React Native Documentation](https://reactnative.dev/)
- [NativeWind Documentation](https://www.nativewind.dev/)
- [Supabase Documentation](https://supabase.com/docs)
- [Expo Router Documentation](https://docs.expo.dev/routing/introduction/)