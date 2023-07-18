This RegEx selects the numbers and decimal separator tfrom a price information in euros (€) within any given text.
- The decimal separator can be either a comma or a dot.
- The euro sign (€) can appear before or after the numbers.
- The space between € sign and the numbers is not an issue.

```
.*?(?:€\s*)?(\d+(?:[,.]\d+)?)\s*(?:€)?.*?
```

## Sample Inputs:
```html
1. <span class="a-price aok-align-center" data-a-size="xl" data-a-color="base"><span class="a-offscreen">299,00€</span>
2. <span class="a-price aok-align-center" data-a-size="xl" data-a-color="base"><span class="a-offscreen">299,00 €</span>
3. <span class="a-price aok-align-center" data-a-size="xl" data-a-color="base"><span class="a-offscreen">299.00€</span>
4. <span class="a-price aok-align-center" data-a-size="xl" data-a-color="base"><span class="a-offscreen">299.00 €</span>
5. <span class="a-price aok-align-center" data-a-size="xl" data-a-color="base"><span class="a-offscreen">€299,00</span>
6. <span class="a-price aok-align-center" data-a-size="xl" data-a-color="base"><span class="a-offscreen">€ 299,00</span>
7. <span class="a-price aok-align-center" data-a-size="xl" data-a-color="base"><span class="a-offscreen">€299.00</span>
8. <span class="a-price aok-align-center" data-a-size="xl" data-a-color="base"><span class="a-offscreen">€ 299.00</span>
```
## Output will always be:
299.00 or 299,00
