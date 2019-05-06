# 16. Retailer display

## The solution

Restyled the #retailer-section with

```css
#retailer-section {
    margin: 45px 0;
    padding: 20px;
}

#retailer-section h2 {
    text-align: center;
}

.retailer__list {
    margin-top: 30px;
    margin-left: auto;
    margin-right: auto;
    width: 90%;
    text-align: center;
}

.retailer__item {
    display: inline-block;
    text-align: center;
    width: 30%;
}

.retailer__item img {
    width: 80%;
    border-radius: 50%;
    border: 2px solid #EC9A29;
}

.retailer__item address {
    text-align: left;
    margin-top: 20px;
    padding-left: 80px;
}
```