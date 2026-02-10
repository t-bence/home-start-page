# Home Start Page

A simple static web page served in a Docker container.

## Quick Start

### Using Docker Compose (Recommended)

```bash
docker-compose up
```

Visit `http://localhost` in your browser.

### Using Docker CLI

```bash
docker build -t home-page .
docker run -p 80:80 -v $(pwd):/usr/share/nginx/html/ home-page
```

## Features

- Simple, clean HTML page with a modern gradient background
- Responsive design that works on mobile and desktop
- Editable files stored in a volume - changes are reflected immediately
- Lightweight nginx-based setup

## Editing

Simply edit `index.html` and `styles.css` in your workspace. Changes will be reflected in the browser (you may need to refresh the page or clear the cache).

## Stopping

```bash
docker-compose down
```

## Template for compose.yml

```yaml
services:
  home-start-page:
    build: .
    ports:
      - "80:80"
    volumes:
      - ./:/usr/share/nginx/html/
```
