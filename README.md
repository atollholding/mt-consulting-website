# MT Consulting information website

## Contents

This repository contains website with public information that the company "MT Consulting" is required to publish online in order to comply with the Ukrainian regulations for joint stock companies.

## How to Use

### Prerequisites

- Ensure you have [Hugo](https://gohugo.io/getting-started/installing/) installed.
- Git should be installed and configured on your system.

### Setup

1. **Clone the Repository**

   ```sh
   git clone --recurse-submodules https://github.com/atollholding/mt-consulting-website.git
   cd mt-consulting-website
   ```

   Note: The `--recurse-submodules` flag is important as it ensures that the PaperMod theme submodule is also cloned.

2. **Initialize and Update Submodules**

   If you have already cloned the repository without the `--recurse-submodules` flag, initialize and update the submodules manually:

   ```sh
   git submodule init
   git submodule update
   ```

### Running the Website Locally

1. **Start the Hugo Server**

   ```sh
   hugo server
   ```

2. **Access the Local Development Server**

   Open your web browser and navigate to `http://localhost:1313` to see the website.

### Making Changes

1. **Editing Content**

   - All content files are located in the `content` directory.
   - Make changes to the markdown files as needed.

2. **Updating the Theme**

   - If there are updates to the PaperMod theme, you can update the submodule:

     ```sh
     cd themes/PaperMod
     git pull origin master
     cd ../../
     ```

### Deployment

1. **Build the Static Files**

   Run the following command to generate the static files:

   ```sh
   hugo
   ```

   The generated files will be in the `public` directory.

2. **Deploying the Website**

   - You can deploy the `public` directory to your web hosting provider.
   - For GitHub Pages, you can push the contents of the `public` directory to the `gh-pages` branch.

     ```sh
     cd public
     git init
     git remote add origin https://github.com/atollholding/mt-consulting-website.git
     git add .
     git commit -m "Deploy site"
     git push --force origin master:gh-pages
     ```

## PaperMod Theme

This website uses the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme. It is included as a submodule in the `themes` directory. Refer to the [PaperMod documentation](https://github.com/adityatelange/hugo-PaperMod/wiki) for detailed usage and customization instructions.

## Credits

Powered by [Hugo](https://gohugo.io) & [PaperMod](https://github.com/adityatelange/hugo-PaperMod/)
