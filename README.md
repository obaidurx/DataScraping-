# Data Scraping from any Website

---

#### Here we use our example website is : [setapp](https://setapp.com/apps)

## Firstly we used Jquery

1. `const s=document.createElement('script')`
2. `s.src="https://code.jquery.com/jquery-3.6.0.slim.js"`
   > use jquery slim from [jquery](https://code.jquery.com/)
3. `document.getElementsByTagName('head')[0].appendChild(s)`
4. `const $=jQuery`
5. `const items=[]`

6. ```javascript
   $(".all-apps-item").each(function () {
     const item = {};
     item.icon = $(this).find(".all-apps-item__icon").attr("src");
     item.name = $(this).find(".all-apps-item__name").html().trim();
     item.description = $(this)
       .find(".all-apps-item__description")
       .html()
       .trim();
     items.push(item);
   });
   ```

```

7. `console.log(items)`
```
