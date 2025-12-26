Examples of code

```py title="add_numbers.py" linenums="1"
# Function to add two numbers
def add_two_numbers(num1, num2):
    return num1 + num2

# Example usage
result = add_two_numbers(5, 3)
print('The sum is:', result)
```

Code highlighting in JS
```js title="code-examples.js" linenums="1" hl_lines="2-4"
// Function to concatenate two strings
function concatenateStrings(str1, str2) {
  return str1 + str2;
}

// Example usage
const result = concatenateStrings("Hello, ", "World!");
console.log("The concatenated string is:", result);
```

Code highlighting in yaml
```yaml title="mkdocs.yml" linenums="1" 
site_name: My Docs
site_url: http://jaradat.ca
theme:
  name: material
  font:
    text: open sans
    code: Red Hat Mono
  logo: assets/logo.png
  features:
    - navigation.instant
    - navigation.instant.progress
    - navigation.instant.preview
    - navigation.tracking
    - navigation.tabs
  # icon:
    # logo: fontawesome/solid/w
  favicon: assets/favicon.ico
  palette:
    # Dark Mode
    - scheme: slate
      toggle:
        icon: material/weather-sunny
        name: Dark mode
      primary: blue
      accent: deep purple

    # Light Mode
    - scheme: default
      toggle:
        icon: material/weather-night
        name: Light mode
      primary: blue
      accent: deep orange

markdown_extensions:
  # Emoji and icons
  - attr_list
  - pymdownx.emoji:
      emoji_index: !!python/name:material.extensions.emoji.twemoji
      emoji_generator: !!python/name:material.extensions.emoji.to_svg
  # code formatting
  - pymdownx.highlight:
      anchor_linenums: true
      line_spans: __span
      pygments_lang_class: true
  - pymdownx.inlinehilite
  - pymdownx.snippets
  #content tabs
  - pymdownx.superfences:
      custom_fences:
        - name: mermaid
          class: mermaid
          format: !!python/name:pymdownx.superfences.fence_code_format 
  - pymdownx.tabbed:
      alternate_style: true
  #admonitions
  - admonition
  - pymdownx.details
  - pymdownx.superfences

#Footer
copyright: Copyright &copy; 2026 Kareem Jaradat
extra:
  social:
    - icon: fontawesome/brands/mastodon 
      link: https://fosstodon.org/@squidfunk 
    - icon: fontawesome/brands/facebook 
      link: https://fosstodon.org/@squidfunk
```