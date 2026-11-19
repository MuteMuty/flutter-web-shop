# Flutter web shop

**A mock shopping app in Flutter on the DummyJSON API: search products, open their details, fill a cart and switch between shoppers.**

<img src="https://github.com/MuteMuty/src/assets/69723817/1b108e99-2e51-4242-a5ca-0bb42f835d7f" alt="Product list: a search field above a two-column grid of phones, each with a photo, price and name" width="250"/>
<img src="https://github.com/MuteMuty/src/assets/69723817/2be4498c-4f48-4aea-90ce-91611eae05a7" alt="Searching for 'ipho' narrows the grid to the iPhone 9 and iPhone X" width="250"/>
<img src="https://github.com/MuteMuty/src/assets/69723817/2189d9dc-5883-4e28-9a78-50b10e49a06b" alt="Cart: five items with prices and plus and minus buttons for the quantity, and an Order button" width="250"/>
<img src="https://github.com/MuteMuty/src/assets/69723817/ca363d6a-d93e-4ba4-9e8c-c026b78c4a72" alt="Product details for a MacBook Pro: photo carousel, price 1,749 €, rating 4.57, description and an Add to cart button showing 'Added to cart'" width="250"/>

## Why it exists

A Flutter project from 2023 (Feb – Jun) that covers a whole shopping flow. It runs on DummyJSON's public mock data, so it needs no backend of its own.

## How it works

| Folder | What it holds |
|---|---|
| `lib/screens/` | Product list with search, product details with an image carousel and a full-screen view, cart, and user picker |
| `lib/models/` | Product, cart and user models parsed from DummyJSON's JSON |
| `lib/widgets/` | Tiles for products, cart items and users, the search field and a snack bar |

Lists load 10 items at a time with `infinite_scroll_pagination`. The chosen user's id is saved with `shared_preferences`, and the cart screen loads that user's cart from `/carts/user/{id}`.

## Run it

Needs Flutter with Dart 2.19 (the project predates Dart 3).

```sh
flutter pub get
flutter run
```

## Tech

Flutter, Dart, `http`, `cached_network_image`, `infinite_scroll_pagination`, `shared_preferences`. Data from [DummyJSON](https://dummyjson.com).

## Status

Finished in Jun 2023 after testing on an Android device. Not maintained. Made by [Erik Pahor](https://github.com/MuteMuty).
