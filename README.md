# Product 'Add to Cart/Sold Out' Button

Problem: When the product has a price listing of $0.00, the 'Add To Cart' button is grayed out, and reads 'Sold Out' instead. Shari would like this button to be removed/invisible when the product price is set to $0.00. Shari would also like the price to be hidden as well. This will allow her to post gallery works that she cannot yet sell.

## Languages Used

Website is Shopify. Files appear to be HTML and liquid. They are saved as .liquid

## Plan of action

Use an if or if/else statement to hide both price and button.

ex.
 ```
{% if product.price == '0.00' %}
    This product has no price!
{% endif %} <br />
```

or ex.

```
{% for item in product.grid} 
    {% if product.proce == '0.00' %} 
    {% endif %}
{% endfor %}
```

## Solution

Used 

```
{% unless product.price <= 0 %}
 insert variable or object here
{% endunless %}
```