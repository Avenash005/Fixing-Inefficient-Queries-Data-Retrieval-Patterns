# Nexus API Optimization TODO

## Setup (if needed)

- [ ] Ensure .env configured with Neon DATABASE_URL
- [ ] Run `npm install`
- [ ] Run `npx prisma generate`
- [ ] Run `npx prisma db push`
- [ ] Run `npx prisma db seed`
- [ ] Test server: `npm run dev`

## FIX 01: Products Pagination & Sorting

- [x] Update src/products/product.service.js: Implement getProducts with page/limit/sortBy/order, max limit 100, meta
- [x] Update src/products/product.controller.js: Pass validated query params

## FIX 02: Orders N+1 Fix

- [x] Update src/orders/order.service.js: Use include.user, remove loop

## FIX 03: Products Fields Selection

- [x] Update src/products/product.controller.js: Parse/validate fields param
- [x] Update src/products/product.service.js: Apply select if fields provided

## Testing

- [x] Verify query logs: single queries, no N+1
- [x] Test endpoints with params
- [x] Complete
