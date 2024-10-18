# Banners and Announcements

A banner can be added to the top of a Jupyter Book: 

```{figure} banner_mude.png
---
width: 70%
name: banner_mude
---
Example of a banner in the MUDE book.
```

This is a commonly used feature, described in the [Jupyter Book manual here](https://jupyterbook.org/en/stable/web/announcements.html). However, note that if you are using the Sphinx-Thebe interactive Python feature, or other features that customize the top part of a Jupyter Book website (for example, the download page buttons), the banner does not always work. In this case, the banner should be specified using the `announcement` option in the `html_theme_options` setting in the `_config.yml` file:

```
sphinx:
  config:
    ...
    html_theme_options:
      ...
      announcement : "This book is under construction ✍🏻; it's continuously updated from September 2024 through January 2025 📅"
      ...
```

```{tip} 
You should always enclose your announcement in quotes to make it a complete string. Use a different type of quote if your announcement itself contains them (for example, `"like 'this'"`). If you are using HTML elements, it is best to make your announcement a complete HTML tag, not Markdown with HTML inside.

Markdown links do not work in the announcement, requiring you to use HTML!
```

## Known Issue

Note that there seems to be a bug if you only use the `announcement` and `launch_buttons:thebe:true` option; including additional buttons seems to fix this issue (see [Issue 65](https://gitlab.tudelft.nl/mude/book/-/issues/65) in the MUDE book), for example:

```
sphinx:
  config:
    ...
    html_theme_options:
      repository_url: "https://github.com/TeachBooks/mechanics-BSc"
      use_repository_button: true
      use_issues_button : true
      announcement : "This book is under construction ✍🏻; it's continuously updated from September 2024 through January 2025 📅"
      launch_buttons:
        thebe: true
```
