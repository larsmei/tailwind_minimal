# tailwind_minimal
This is my template for a minimal tailwind-setup. Just html and tailwind, no framework.


* How to use this template to create a fresh tailwind-setup
  * install node.js ( latest version )
  * create a folder for your project and use the following commands in this folder
  * clone this repo
    ```shell
      git clone https://github.com/larsmei/tailwind_minimal .
    ```
  * install tailwind
    ```shell
      npx tailwindcss-cli@latest build -o tailwind.css
    ```
  * create configuration
   ```shell
    npx tailwindcss-cli@latest init
    ```    
  * create ouput.css file ( rerun after changing the config )
    ```shell
      npx tailwindcss-cli@latest build ./style.css -o ./output.css
    ```
  * create production-version ( minified css )
    * create purge entry in tailwind.config.js
    ```shell
    module.exports = {
    purge: [
      './*.html',
    ],
    }
    ```
    * rebuild with production env-var
      ``` shell
      NODE_ENV=production npx tailwindcss-cli@latest build ./style.css -o ./output.css
      ```
