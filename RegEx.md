This RegEx selects the numbers that contain price information in euros (€) within any given text. The decimal separator can be either a comma or a dot, and the euro sign (€) can appear before or after the numbers.

```
.*?(?:€\s*)?(\d+(?:[,.]\d+)?)\s*(?:€)?.*?
```

## Sample Input:
```html
<span class="a-price aok-align-center" data-a-size="xl" data-a-color="base"><span class="a-offscreen">299,00€</span>
```
## Output:
299.00
