# Responsive Image Slider with Splide.js

![Slider Preview](https://ogtemplate.com/wp-content/uploads/2025/01/20241013_125830.webp)

A lightweight, responsive image slider/carousel implementation using Splide.js with mobile-optimized design and smooth transitions.

## Features

- 🖼️ **Responsive Image Slider** - Adapts to all screen sizes
- ⏱️ **Auto-Play Functionality** - 3-second interval with pause on hover
- 🔄 **Infinite Loop** - Seamless continuous sliding
- 📱 **Mobile-Optimized** - Different heights for desktop/mobile
- 🎨 **Custom Styled Navigation**
  - Pink/red pagination dots
  - White navigation arrows with hover effects
- 🖱️ **Clickable Slides** - Each image links to external URLs
- 🏗️ **Lazy Loading** - Improved performance

## Installation

No installation required - works as standalone HTML. Just include:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@splidejs/splide@latest/dist/css/splide.min.css">
<script src="https://cdn.jsdelivr.net/npm/@splidejs/splide@latest/dist/js/splide.min.js"></script>
```

## Usage

1. Add the HTML structure:
```html
<div id="splide" class="splide">
  <div class="splide__track">
    <ul class="splide__list">
      <li class="splide__slide">
        <a href="YOUR_LINK"><img src="IMAGE_URL" alt="Description"></a>
      </li>
      <!-- Add more slides -->
    </ul>
  </div>
</div>
```

2. Initialize with JavaScript:
```javascript
new Splide('#splide', {
  type: 'loop',
  perPage: 1,
  autoplay: true,
  interval: 3000,
  pauseOnHover: true,
  lazyLoad: 'nearby'
}).mount();
```

## Customization Options

### Styling
```css
/* Change dot colors */
.splide__pagination__page {
  background-color: #e6b1c1;
}
.splide__pagination__page.is-active {
  background-color: #e61355;
}

/* Adjust heights */
.splide__slide img {
  height: 250px; /* Desktop */
}
@media (max-width: 768px) {
  .splide__slide img {
    height: 100px; /* Mobile */
  }
}
```

### Slider Settings
| Option | Default | Description |
|--------|---------|-------------|
| type | 'loop' | Loop mode (also 'slide'/'fade') |
| interval | 3000 | Autoplay interval in ms |
| pauseOnHover | true | Pause on mouse hover |
| lazyLoad | 'nearby' | Lazy loading strategy |

## Browser Support

Works on all modern browsers including:
- Chrome
- Firefox
- Safari
- Edge
- Mobile browsers
