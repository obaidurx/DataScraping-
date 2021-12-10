# Scraping data from any website

> This is just an example website : [setapp](https://setapp.com/apps)

## For beginning, we used Javascript.

```javascript
const items = [];
```

```javascript
document.querySelectorAll(".all-apps-item").forEach((item) => {
  const _item = {};
  _item.description = item
    .querySelector(".all-apps-item__description")
    .innerHTML.trim();
  _item.name = item.querySelector(".all-apps-item__name").innerHTML.trim();
  _item.icon = item
    .querySelector(".all-apps-item__icon")
    .getAttribute("src")
    .trim();
  items.push(_item);
});
```

```javascript
console.log(items);
```

## Next, we used Jquery.

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

---

**Hasin hayder vai** deserved all the credit.
