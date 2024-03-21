# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

- Configure the top-level `parserOptions` property like this:

```js
export default {
  // other rules...
  parserOptions: {
    ecmaVersion: 'latest',
    sourceType: 'module',
    project: ['./tsconfig.json', './tsconfig.node.json'],
    tsconfigRootDir: __dirname,
  },
};
```

- Replace `plugin:@typescript-eslint/recommended` to `plugin:@typescript-eslint/recommended-type-checked` or `plugin:@typescript-eslint/strict-type-checked`
- Optionally add `plugin:@typescript-eslint/stylistic-type-checked`
- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and add `plugin:react/recommended` & `plugin:react/jsx-runtime` to the `extends` list

# Adding eslint airbnb config

-Delete eslint file default

## Install the following packages:

```bash
npx eslint --init
```

### Select :

```bash
   ✔ How would you like to use ESLint? · problems
    ✔ What type of modules does your project use? · esm
    ✔ Which framework does your project use? · react
    ✔ Does your project use TypeScript? · No / Yes
    ✔ Where does your code run? · browser
    ✔ What format do you want your config file to be in? · JavaScript
```

## Add airbnb config:

```bash
 npm @typescript-eslint/eslint-plugin@latest eslint-plugin-react@latest @typescript-eslint/parser@latest
```

## Add typescript suport:

```bash
npx install-peerdeps --dev eslint-config-airbnb
```

## Adding the rest of the packages:

```bash
npm i -D eslint-config-airbnb-typescript
npm i -D prettier eslint-config-prettier eslint-plugin-prettier
npm i -D vitest
npm i -D @testing-library/react @testing-library/jest-dom @testing-library/user-event jsdom
npm i -D @vitest/coverage-v8 @vitest/ui
npm install --save-dev @commitlint/config-conventional @commitlint/cli
```

## Important!:

- Add "types": ["vitest/globals"] to your tsconfig.json file
