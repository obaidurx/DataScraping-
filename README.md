# Data Scraping from any Website

> Here we use our example website is : [setapp](https://setapp.com/apps)

## Firstly we used Jquery

```javascript
const s = document.createElement("script");
```

```javascript
s.src = "https://code.jquery.com/jquery-3.6.0.slim.js";
```

> use jquery slim from [jquery](https://code.jquery.com/)

```javascript
document.getElementsByTagName("head")[0].appendChild(s);
```

```javascript
const $ = jQuery;
```

```javascript
const items = [];
```

```javascript
$(".all-apps-item").each(function () {
  const item = {};
  item.icon = $(this).find(".all-apps-item__icon").attr("src");
  item.name = $(this).find(".all-apps-item__name").html().trim();
  item.description = $(this).find(".all-apps-item__description").html().trim();
  items.push(item);
});
```

```javascript
console.log(items);
```
