# Amazon Sales Dashboard Documentation

## 1. Folder Contents

This folder contains the complete client presentation package.

| File | Purpose |
|---|---|
| `amazon.final.html` | Main interactive dashboard file. Open this file in a browser to present the dashboard. |
| `amazon.csv` | Source product dataset used as the reference data file for the Amazon product analysis. |
| `Dashboard_Documentation.md` | Explanation of included files, dashboard sections, calculations, and interactions. |

Important note: the dashboard is a self-contained HTML presentation file. It does not need a server to run. The summarized metrics are embedded inside the HTML so the dashboard loads quickly and works offline.

## 2. Data Source

The included `amazon.csv` file contains Amazon product-level data with columns such as:

| Column | Meaning |
|---|---|
| `product_id` | Unique product identifier. |
| `product_name` | Product title/name. |
| `category` | Product category path. |
| `discounted_price` | Selling price after discount. |
| `actual_price` | Original listed price before discount. |
| `discount_percentage` | Discount percentage offered. |
| `rating` | Product rating. |
| `rating_count` | Number of reviews/ratings. |
| `about_product` | Product description. |
| `review_title` | Review headline text. |
| `review_content` | Review content text. |
| `img_link` | Product image URL. |
| `product_link` | Amazon product URL. |

## 3. Dashboard Technology

The dashboard is built as a single HTML file using:

| Technology | Usage |
|---|---|
| HTML | Page structure, dashboard tabs, cards, tables, and drilldown panels. |
| CSS | Professional dark theme, responsive layout, cards, buttons, charts, and presentation styling. |
| JavaScript | Data handling, tab switching, filters, click interactions, and metric updates. |
| Chart.js | Bar charts, doughnut charts, scatter charts, and bubble charts. |
| Google Fonts | Dashboard typography using Plus Jakarta Sans, Outfit, and JetBrains Mono. |

## 4. Dashboard Sections

### 4.1 Sales Overview

This is the main landing section for the client presentation.

It includes:

| Metric | Meaning |
|---|---|
| Total Products | Total number of products analyzed. |
| Total Reviews | Total review/rating volume across products. |
| Average Rating | Mean customer rating across products. |
| Average Discount | Average discount percentage across products. |
| Average Savings | Average price saving per product. |

Charts and visual blocks included:

| Visual | Explanation |
|---|---|
| Products by Category | Shows product count across major categories. Clicking a category opens a detail panel. |
| Review Share | Doughnut chart showing review distribution by category. |
| Average Discount by Category | Compares average discount percentage category-wise. |
| Rating Distribution | Shows how products are distributed across rating bands. |
| Price Value Chain | Shows the flow from list price to discount, sale price, savings, rating, and reviews. |
| Discount Bucket Distribution | Shows how many products fall into each discount band. |
| Review Volume by Category | Interactive bar list showing review concentration by category. |

### 4.2 Directional Sales View

This is the new professional regional sales panel added for client presentation.

Regions included:

| Direction | Region |
|---|---|
| N | North |
| S | South |
| E | East |
| W | West |
| C | Central |

When the user clicks a direction, the dashboard updates:

| Metric | Meaning |
|---|---|
| Total Sales | Total regional sales value. |
| Average Sales | Average sales value per sales order. |
| Particular Sales | Sales value for the leading category in that region. |
| Sales Orders | Number of sales orders used for that regional summary. |
| Top Category | Best performing category in that region. |
| Average Discount | Average regional discount percentage. |
| Rank | Region rank based on total sales. |
| Category Mix | Breakdown of sales by category inside the selected region. |

Note: the original CSV is product/catalog data and does not contain geographic sales transactions. Therefore, this regional sales model is embedded in the dashboard as a presentation-ready business view.

### 4.3 Category Deep Dive

This section analyzes category-level performance.

It includes:

| Item | Explanation |
|---|---|
| Category Cards | Clickable cards for each category. |
| Product Count | Number of products in the category. |
| Review Volume | Total reviews in the category. |
| Review Share | Category review percentage compared with total reviews. |
| Average Discount | Category-level discount average. |
| Average Rating | Category-level customer rating average. |
| Price Analysis | Average list price, average sale price, and average savings. |
| Catalog Share | Category share of total product count and review count. |

### 4.4 Pricing and Discount Analysis

This section focuses on pricing behavior.

It includes:

| Metric | Meaning |
|---|---|
| Highest Discount | Maximum discount percentage observed. |
| Highest Price | Highest listed product price. |
| Most Affordable | Lowest product selling price. |
| Above 60 Percent Discount | Share of products with high discounting. |

Charts included:

| Visual | Explanation |
|---|---|
| Discount Heatmap by Category | Shows which categories are aggressively discounted. |
| Price Range Distribution | Shows how products are distributed across price bands. |
| Discount Buckets | Groups products by discount percentage range. |
| Actual vs Discounted Price | Compares average original and selling price. |
| Savings Opportunity | Highlights where price savings are highest. |

### 4.5 Ratings and Reviews Intelligence

This section focuses on customer quality signals.

It includes:

| Metric | Meaning |
|---|---|
| Products >= 4 Stars | Count and percentage of highly rated products. |
| Max Reviews | Product with the highest review count. |
| Best Average Rating | Highest performing product/category by rating. |
| Rated Below 3 Stars | Count of low-rated products. |

Charts included:

| Visual | Explanation |
|---|---|
| Rating Distribution Deep Dive | Shows counts across rating bands. |
| Quality Scorecard | Shows rating quality indicators. |
| Average Rating by Category | Compares ratings across categories. |
| Review Volume Leaders | Highlights categories/products with strongest review volume. |

### 4.6 Top Products Leaderboard

This section lists top products and supports filtering.

It includes:

| Feature | Explanation |
|---|---|
| Search Box | Search products by name or category. |
| Category Filters | Filter by All, Electronics, Computers, or Home & Kitchen. |
| Product Table | Displays product name, category, rating, reviews, sale price, list price, discount, and savings. |
| Product Drilldown | Clicking a row opens detailed product information. |
| Top 10 by Reviews | Chart of highest review-count products. |
| Top 10 by Discount | Chart of products with strongest discounts. |

### 4.7 Key Insights and Findings

This section summarizes business interpretation.

Main insight areas:

| Insight Area | Explanation |
|---|---|
| Discount Strategy | Shows discount patterns and aggressive pricing areas. |
| Quality Signals | Explains rating strength and review concentration. |
| Market Concentration | Identifies categories dominating product and review share. |
| Discount vs Rating Correlation | Shows whether high discounting affects ratings. |
| Top Opportunities | Lists strategic actions and business opportunities. |

## 5. Main Formulas and Calculations

### 5.1 Total Products

Formula:

```text
Total Products = Count of all product rows
```

Dashboard value:

```text
1,465 products
```

### 5.2 Total Reviews

Formula:

```text
Total Reviews = Sum of rating_count across all products
```

Dashboard value:

```text
26.7M reviews
```

### 5.3 Average Reviews Per Product

Formula:

```text
Average Reviews Per Product = Total Reviews / Total Products
```

Example:

```text
26.7M / 1,465 = approx. 18.2K reviews per product
```

### 5.4 Average Rating

Formula:

```text
Average Rating = Sum of product ratings / Number of rated products
```

Dashboard value:

```text
4.08
```

### 5.5 Average Discount

Formula:

```text
Average Discount = Sum of discount percentages / Number of products
```

Dashboard value:

```text
47.5%
```

### 5.6 Savings Per Product

Formula:

```text
Savings = Actual Price - Discounted Price
```

Average savings formula:

```text
Average Savings = Average Actual Price - Average Discounted Price
```

Dashboard value:

```text
Approx. INR 1.2K average savings per product
```

### 5.7 Review Share by Category

Formula:

```text
Category Review Share = Category Reviews / Total Reviews * 100
```

Example:

```text
Electronics Review Share = Electronics Reviews / Total Reviews * 100
```

### 5.8 Category Product Share

Formula:

```text
Category Product Share = Category Products / Total Products * 100
```

### 5.9 Category Average Discount

Formula:

```text
Category Average Discount = Sum of discounts in category / Number of products in category
```

### 5.10 Category Average Sale Price

Formula:

```text
Category Average Sale Price = Sum of discounted prices in category / Number of products in category
```

### 5.11 Category Average List Price

Formula:

```text
Category Average List Price = Sum of actual prices in category / Number of products in category
```

### 5.12 Category Average Savings

Formula:

```text
Category Average Savings = Category Average List Price - Category Average Sale Price
```

### 5.13 Rating Bucket Percentage

Formula:

```text
Rating Bucket Percentage = Products in Rating Bucket / Total Rated Products * 100
```

Example rating buckets:

```text
< 2
2-3
3-3.5
3.5-4
4-4.5
4.5-5
```

### 5.14 Discount Bucket Percentage

Formula:

```text
Discount Bucket Percentage = Products in Discount Bucket / Total Products * 100
```

Example discount buckets:

```text
0-20%
20-40%
40-60%
60-80%
80-100%
```

### 5.15 Price Range Percentage

Formula:

```text
Price Range Percentage = Products in Price Range / Total Products * 100
```

Example price ranges:

```text
INR 0-500
INR 500-2K
INR 2K-5K
INR 5K-15K
INR 15K-50K
INR 50K+
```

## 6. Directional Sales Formulas

The Directional Sales View uses region-level sales summary values embedded in the dashboard.

### 6.1 Total Regional Sales

Formula:

```text
Total Regional Sales = Sum of all sales for the selected region
```

### 6.2 Average Regional Sales

Formula:

```text
Average Regional Sales = Total Regional Sales / Number of Sales Orders
```

Example:

```text
North Average Sales = North Total Sales / North Sales Orders
```

### 6.3 Particular Sales

Formula:

```text
Particular Sales = Sales from the top performing category in the selected region
```

Example:

```text
North Particular Sales = Electronics sales in North
```

### 6.4 Regional Sales Share

Formula:

```text
Regional Sales Share = Selected Region Sales / Total Sales Across All Regions * 100
```

### 6.5 Regional Rank

Formula:

```text
Regional Rank = Position of selected region after sorting all regions by total sales descending
```

### 6.6 Regional Category Mix

Formula:

```text
Category Mix Percentage = Category Sales in Region / Top Category Sales in Region * 100
```

This controls the horizontal bar width inside the selected region's category breakdown.

## 7. Dashboard Interactions

| Interaction | Result |
|---|---|
| Click Overview tab | Shows summary KPIs and main sales overview. |
| Click Categories tab | Shows category-level deep dive. |
| Click Pricing & Discounts tab | Shows pricing and discount analysis. |
| Click Ratings & Reviews tab | Shows rating and review intelligence. |
| Click Top Products tab | Shows searchable product leaderboard. |
| Click Insights tab | Shows strategic business findings. |
| Click a direction card | Updates regional sales metrics, rank, sales chart, and category mix. |
| Click a category chart bar | Opens category drilldown. |
| Click a category card | Updates category detail panel. |
| Search product table | Filters product rows by matching text. |
| Click product filter buttons | Filters product table by selected category. |
| Click product row | Opens product detail drilldown. |

## 8. Presentation Talking Points

Recommended client presentation flow:

1. Start with Sales Overview to introduce total catalog size, reviews, rating, discount, and savings.
2. Use Directional Sales View to explain North, South, East, West, and Central performance.
3. Click North or West to demonstrate interactive region-level analysis.
4. Move to Category Deep Dive to show product concentration and review share.
5. Use Pricing & Discount Analysis to explain pricing strategy.
6. Use Ratings & Reviews Intelligence to explain customer quality signals.
7. Use Top Products Leaderboard for product-level proof.
8. End with Key Insights & Findings for business recommendations.

## 9. Design Theme

The dashboard uses a professional dark analytics theme suitable for client presentation.

Design choices:

| Design Area | Explanation |
|---|---|
| Background | Dark executive dashboard style instead of plain white. |
| Cards | Clean bordered cards with subtle depth. |
| Colors | Distinct colors for sales, reviews, ratings, discount, and region selection. |
| Typography | Strong dashboard typography for better readability. |
| Layout | Wide dashboard layout optimized for presentation screens. |
| Live Badge | Removed to make the dashboard look like a polished client-ready report, not a live system mockup. |

## 10. How to Run

1. Open the folder `Amazon_Sales_Dashboard_Client_Presentation`.
2. Double-click `amazon.final.html`.
3. The dashboard will open in your browser.
4. Use the top tabs and clickable cards during the presentation.

No installation is required.

## 11. Important Notes

- The dashboard is designed for presentation and analysis storytelling.
- The CSV is included for transparency and source reference.
- The HTML contains embedded summary values so it can run offline.
- The directional sales view is an added regional business layer for client presentation.
- If exact geographic sales must be calculated from raw data in the future, the CSV needs region/location/sales-order fields.

