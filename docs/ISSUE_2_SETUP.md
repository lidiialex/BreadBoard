# Project Setup Guide for BreadBoard

## Issue #2: Project Setup

This guide will walk you through the process of setting up the BreadBoard project, including steps for environment setup, TypeScript configuration, Vite configuration, project structure, and troubleshooting.

### 1. Environment Setup

#### Prerequisites
- **Node.js**: Ensure you have Node.js (v14 or higher) installed. You can download it from [nodejs.org](https://nodejs.org/).
- **Package Manager**: We recommend using npm or yarn as your package manager.

#### Steps
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/lidiialex/BreadBoard.git
   cd BreadBoard
   ```
2. **Install Dependencies**:
   ```bash
   npm install
   ```
   or if using yarn:
   ```bash
   yarn install
   ```

### 2. TypeScript Configuration

The BreadBoard project uses TypeScript for type safety. To set up TypeScript:

1. **Install TypeScript**:
   ```bash
   npm install typescript --save-dev
   ```
2. **Create a tsconfig.json file** (if it doesn’t exist):
   ```bash
   npx tsc --init
   ```
3. **Configure tsconfig.json**: Ensure the following settings are included:
   ```json
   {
     "compilerOptions": {
       "target": "ES6",
       "module": "ESNext",
       "strict": true,
       "esModuleInterop": true,
       "skipLibCheck": true,
       "forceConsistentCasingInFileNames": true
     }
   }
   ```

### 3. Vite Configuration

BreadBoard uses Vite for fast development and build process.

1. **Install Vite**:
   ```bash
   npm install vite --save-dev
   ```
2. **Create a vite.config.ts file** (if it doesn’t exist):
   ```ts
   import { defineConfig } from 'vite';
   import vue from '@vitejs/plugin-vue';

   export default defineConfig({
     plugins: [vue()]  
   });
   ```
3. **Run Vite**:
   ```bash
   npx vite
   ```

### 4. Project Structure

Your project structure should look like this:
```
BreadBoard/
├── docs/
│   └── ISSUE_2_SETUP.md
├── src/
│   ├── main.ts
│   └── components/
├── public/
├── package.json
├── tsconfig.json
└── vite.config.ts
```

### 5. Troubleshooting

- **Node Version Issues**: Ensure you’re running a supported version of Node.js. You can check your version with `node -v`.
- **Module Not Found**: If you encounter errors about modules not found, try deleting `node_modules` and `package-lock.json`, then run `npm install` again.
- **Vite Not Starting**: Ensure Vite is properly installed and your configuration is correct. Check for syntax errors in `vite.config.ts`.
- **Type Errors**: Review TypeScript errors carefully; they often provide hints on how to resolve the issues.

---

For more information, refer to the [Vite Documentation](https://vitejs.dev/guide/) and the [TypeScript Handbook](https://www.typescriptlang.org/docs/).