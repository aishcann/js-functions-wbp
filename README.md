# JS Functions WBP

Possible solutions below. If you got the same answer but through a different method, all is well! There are many different ways to solve problems in code.

## Step 1

```JS
function previewFullPrice(salesTax, shippingPrice) {
  const shirtPrice = 30.99;
  const sweatshirtPrice = 40.99;
  const smallPosterPrice = 15.99;
  const largePosterPrice = 22.99;
  const mugPrice = 12.99;

  function priceCalculation (item) {
      itemPriceAfterTax = item * (1 + salesTax);
			itemPriceAfterShipping = itemPriceAfterTax + shippingPrice;
			itemPriceAfterShippingRounded = itemPriceAfterShipping.toFixed(2);
      return itemPriceAfterShippingRounded
  }

  shirtPriceAfterShippingRounded = priceCalculation(shirtPrice);
  sweatshirtPriceAfterShippingRounded = priceCalculation(sweatshirtPrice)
  smallPosterPriceAfterShippingRounded = priceCalculation(smallPosterPrice)
  largePosterPriceAfterShippingRounded = priceCalculation(largePosterPrice);
  mugPriceAfterShippingRounded = priceCalculation(mugPrice);

  return [
    shirtPriceAfterShippingRounded,
    sweatshirtPriceAfterShippingRounded,
    smallPosterPriceAfterShippingRounded,
    largePosterPriceAfterShippingRounded,
    mugPriceAfterShippingRounded,
  ];
}
```
## Step 2

```JS
function capitalize (words) {
   return words.map((word) => word.charAt(0).toUpperCase() + word.substring(1));
  }
    

function formatProducts(carousel, grid, sidebar) {
  const carouselProductsReformatted = carouselProducts.map((product) => {
    // replace underscores with spaces
    let spacedProduct = product.replace("_", " ");

    //capitalize each word
    productWords = spacedProduct.split(" ");
    capitalizedProductWords = capitalize(productWords)
    capitalizedProduct = capitalizedProductWords.join(" ");
    return capitalizedProduct;
  });

  const gridProductsReformatted = gridProducts.map((product) => {
    // replace underscores with spaces
    let spacedProduct = product.replace("_", " ");

    //capitalize each word
    productWords = spacedProduct.split(" ");
    capitalizedProductWords = capitalize(productWords);
    capitalizedProduct = capitalizedProductWords.join(" ");
    return capitalizedProduct;
  });

  const sidebarProductsReformatted = sidebarProducts.map((product) => {
    // replace underscores with spaces
    let spacedProduct = product.replace("_", " ");

    //capitalize each word
    productWords = spacedProduct.split(" ");
    capitalizedProductWords = capitalize(productWords);
    capitalizedProduct = capitalizedProductWords.join(" ");
    return capitalizedProduct;
  });

  return [
    carouselProductsReformatted,
    gridProductsReformatted,
    sidebarProductsReformatted,
  ];
}
```

## Step 3

```JS
function greetingGenerator(customerName, storeName) {
  let greeting = "";

  const hello = function () {
    return 'Hello ';
  };

  function welcome() {
    return 'Welcome to the ';
  }

  function store(storeName) {
    return `${storeName}!`;
  }

  const customer = (customer) => `${customer}! `;

  greeting += hello();
  greeting += customer(customerName);
  greeting += welcome();
  greeting += store(storeName);

  return greeting;
}
```

## Step 4
```JS
function areAllIdsUnique(allIds) {
  for (let id of allIds) {
    const isThisIdUnique = isUnique(allIds, id);
    if (!isThisIdUnique) {
      return false;
    }
  }
  return true;
}
```