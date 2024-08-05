name: Build ReactJS

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

jobs:
  build:
    name: Vite build
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repo
        uses: actions/checkout@v4.1.7

      - name: Setup Node
        uses: actions/setup-node@v4.0.3

      - name: Install dependencies
        run: npm install

      - name: Build project
        run: npm run build

      - name: Upload production-ready build files
        uses: actions/upload-artifact@v4.3.4
        with:
          name: production-files
          path: ./dist
