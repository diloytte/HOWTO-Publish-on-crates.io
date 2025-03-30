# HOWTO-Publish-on-crates.io

1. Go to website: https://crates.io/

2. Click **Login With Github** (top-right corner).

3. Once loged in:
   - Click on your account icon.
   - Go to **Account Setting**.
   - Select **API Tokens**.
   - Create new token by giving it a _name_ and _permissions_ (select all most of the time).
   - Click __Generate Token__

4. Go to your terminal.
   - type `cargo login`.
   - paste the API Token text.
  
5. Start a new project by writing: `cargo new <project_name> --lib`

6. Write code...

7. In `Cargo.toml` in `[package]` section, add:  
   - `authors`  
       Example: authos = ["mail@diloytte.com"]
   - `license`  
       Example: license = "MIT"
   - `repository`  
       Example: repository = "https://github.com/diloytte/HOWTO-Publish-on-crates.io"
   - `homepage`  
       Example: homepage = "https://www.dilloyte.com' or just use github repo as a link.
   - `readme`  
       Example: readme = "README.md"
   - `keywords`  
       Example: keywords = ["how to, project, something"]
   -  `categories`  
       Example: keywords = ["category1, category2"]  
       Visit: httpps://crates.io/category_slugs for finding the categories.

8. Once publish is ready, execute: `cargo publish --dry-run`,  
   this is command that will not publish, but this is just a 'test publish' to see if there are any errors to fix.

9. If all checks pass, publish crate using `cargoo publish`.
