# Minimola

Minimola is a [Minima v2](https://github.com/jekyll/minima) Clone originally based on [Even](https://www.getzola.org/themes/even/) is a clean, responsive theme featuring categories, tags and pagination.

## Contents

- [Installation](#installation)
- [Options](#options)
  - [Top menu](#top-menu)
  - [Title](#title)

## Installation
First download this theme to your `themes` directory:

```bash
cd themes
git clone https://github.com/1peter10/minimola.git
```
and then enable it in your `config.toml`:

```toml
theme = "even"
```

The theme requires tags and categories taxonomies to be enabled in your `config.toml`:

```toml
taxonomies = [
    # You can enable/disable RSS
    {name = "categories", feed = true},
    {name = "tags", feed = true},
]
```
If you want to paginate taxonomies pages, you will need to overwrite the templates
as it only works for non-paginated taxonomies by default.

It also requires to put the posts in the root of the `content` folder and to enable pagination, for example in `content/_index.md`:

```
+++
paginate_by = 5
sort_by = "date"
+++
```

## Options

### Top-menu
Set a field in `extra` with a key of `blog_menu`:

```toml
# This is the default menu
blog_menu = [
    {url = "$BASE_URL", name = "Home"},
    {url = "$BASE_URL/categories", name = "Categories"},
    {url = "$BASE_URL/tags", name = "Tags"},
    {url = "$BASE_URL/about", name = "About"},
]
```

If you put `$BASE_URL` in a url, it will automatically be replaced by the actual
site URL.

### Title
The site title is shown on the header. As it might be different from the `<title>`
element that the `title` field in the config represents, you can set the `even_title`
instead.

### More documentation
Check the comments in [config.toml](config.toml), or open an [Issue](https://github.com/1peter10/minimola/issues)!
