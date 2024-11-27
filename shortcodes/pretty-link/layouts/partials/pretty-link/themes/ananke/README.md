# Pretty Link: Ananke

Ananke manages styles through a separate `custom.css` file. Please configure `custom_css` as shown in the code below.

The `custom.css` file should be located at `/assets/css/custom.css`.

> The styles are a simplified and slightly modified version of TailwindCSS. While they are not fully optimized, contributions via Pull Requests are welcome!

**hugo.toml**
```toml
baseURL = 'https://example.org/'
languageCode = 'en-us'
title = 'Ananke Pretty Link'
theme = 'ananke'

#################################################################
# Add the following lines of code.
[params]
custom_css = ["custom.css"]
favicon = "/images/favicon.ico"

# pretty_link
[params.pretty_link]
theme = "ananke"

[[module.imports]]
path = "github.com/mariox77/hugo-modules/shortcodes/pretty-link"
```

**/assets/css/custom.css**
```css
.anchor-card {
  text-decoration: none;
  color: black;
  margin: 1rem;
}

.card {
  display: flex;
  flex-direction: column;
  border: 1px solid #e5e7eb;
  background-color: rgba(243, 244, 246, 0.4);
  overflow: hidden;
  transition: transform 0.3s, box-shadow 0.3s;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  max-width: 100%;
}

.card:hover {
  background-color: #ffffff;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.thumbnail {
  flex-grow: 0;
  width: 100%;
  max-height: 16rem;
  background-color: #fafafa;
  overflow: clip;
  margin: 0;
  border-radius: 0;
  transition: transform 0.3s;
}

.object-cover {
  object-fit: cover;
}

.object-scale-down {
  object-fit: scale-down;
}

.py-3 {
  padding: 0.75rem 0rem;
}

.card:hover .thumbnail {
  transform: scale(1.05);
}

.content {
  display: flex;
  flex: 1;
  flex-direction: column;
  padding: 0.5rem 1rem;
  gap: 0.25rem;
  max-width: 100%;
  height: 100%;
  overflow: hidden;
}

.title-wrapper {
  display: flex;
  align-items: center;
  font-weight: bold;
  font-size: 1rem;
  color: #111827;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  width: 100%;
  max-width: 100%;
}

.favicon {
  flex-shrink: 0;
  width: 1.25rem;
  height: 1.25rem;
  margin: 0;
}

.title {
  font-weight: bold;
  font-size: 1rem;
  margin-left: 0.5rem;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  max-width: 100%;
}

.summary-wrapper {
  flex: 1 1 0%;
  padding-bottom: 0.5rem;
  width: 100%;
  max-width: 100%;
}

.summary {
  font-size: 0.875rem;
  color: rgba(17, 24, 39, 0.9);
  line-height: 1.5rem;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
}

.permalink {
  font-size: 0.75rem;
  color: rgba(107, 114, 128, 0.5);
  text-align: right;
  align-self: flex-end;
  max-width: 24rem;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}

@media (min-width: 768px) {
  .thumbnail {
    width: 15rem;
    min-width: 15rem;
  }

  .card {
    flex-direction: row;
    height: 8rem;
    margin: 0 1rem;
  }

  .permalink {
    font-size: 0.625rem;
  }
}
```
