# Product Availability & Inventory Model

**Tools:** Microsoft Excel (XLOOKUP, VLOOKUP, Advanced Formulas, Combinatorial Logic)  
**Context:** Built at LongCap Lamson Products LLC to support weekly inventory tracking and WooCommerce stock management

---

## Overview

This Excel-based inventory management model was developed to:

- Track real-time stock levels across individual items and product sets (multi-component bundles)
- Determine how many complete sets can be assembled from available component inventory
- Synchronize accurate stock counts to the WooCommerce DTC website

The model handles both **purchased (P)** and **manufactured (M)** goods across multiple product categories including Utensils, Servers, Protection, and Trade Tools.

---

## Key Features

### Set Availability Calculation
- Identifies which SKUs are sets vs. individual items using an EA/SET flag
- Reads component SKU combinations from a CONTAINS column
- Calculates how many complete sets can be assembled based on the minimum available quantity across all required components

### Inventory Tracking
- Tracks Day of Week (DOW) count schedules per SKU
- Maintains actual physical count, adjusted stock count, and website-ready stock columns
- Flags low stock items automatically based on configurable minimum quantity thresholds
- Identifies discontinued and out-of-stock items

### WooCommerce Sync Workflow
- Structured process to download WooCommerce stock data, reconcile with physical counts, calculate adjusted values, and upload updated stock in CSV format
- XLOOKUP and VLOOKUP-based data mapping between WooCommerce exports and the inventory template

### Formula Sheet
- Contains reusable lookup formulas including XLOOKUP with SUBSTITUTE logic for SKU standardization across product lines

---

## Workflow

1. Download stock data from WooCommerce
2. Map downloaded data to inventory template using VLOOKUP
3. Filter by day of week and sort by SKU — print for physical count
4. Filter stock column to items at or below threshold — print low stock report
5. Conduct warehouse physical count
6. Input actual counts into the model
7. Apply adjusted stock formula
8. Export SKU and adjusted stock columns as CSV and upload to WooCommerce

---

## Business Impact

- Eliminated manual set availability calculations across multi-component product bundles
- Reduced risk of overselling sets when individual components were low in stock
- Standardized the weekly inventory reconciliation and website update process
- Supported accurate stock representation across the DTC WooCommerce storefront
