<<<<<<< HEAD
This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
=======
# 2X STORE
## Product Requirements Document
### E-Commerce Website — Phase 1

---

| | | | |
|---|---|---|---|
| **Version** 1.0 | **Status** Draft | **Market** Egypt (EG) | **Phase** Phase 1 / MVP |

---

## 1. Product Overview

2X Store is a men's fashion e-commerce website targeting Egyptian customers aged 18–45. The platform will serve as the brand's primary digital storefront, offering streetwear, casual, and formal clothing with a curated catalog of 50–100 products at launch.

The checkout model is WhatsApp-based: instead of an integrated payment gateway, customers build a cart on the website and are redirected to WhatsApp with a pre-filled order message sent to the store owner. This approach keeps operations lean, maintains a personal sales relationship, and allows the brand to validate demand before investing in full payment infrastructure.

The platform is designed from the ground up to be scalable — with real payment processing, order tracking, push notifications, and a mobile app all identified as Phase 2 priorities.

| Field | Value |
|---|---|
| Product Name | 2X Store — E-Commerce Website |
| Platform | Web (Responsive — Desktop & Mobile) |
| Target Market | Egypt — Arabic-speaking men, ages 18–45 |
| Language | Arabic UI / English product details, sizes, colors, numbers |
| Checkout Model | WhatsApp-based (no payment gateway in Phase 1) |
| Catalog Size | 50–100 products at launch |
| Admin | Single admin panel for store owner |

---

## 2. Goals & Success Metrics

### 2.1 Business Goals

- Establish 2X Store's digital presence with a professional, brand-aligned website
- Enable customers to browse and purchase via a familiar WhatsApp-based flow
- Give the store owner full control over catalog, inventory, and promotions
- Build a scalable technical foundation ready for Phase 2 upgrades

### 2.2 Success Metrics (Phase 1)

| Metric | Target | Timeframe |
|---|---|---|
| WhatsApp order conversions | 50+ orders/month | Month 2 |
| Registered user accounts | 200+ accounts | Month 3 |
| Average session duration | > 2 minutes | Month 1 |
| Mobile traffic share | > 70% | Ongoing |
| Product page load time | < 2 seconds | Launch |

---

## 3. Target Users

### 3.1 End Customer

- Egyptian men, ages 18–45
- Style preferences: streetwear, casual, and formal
- Primarily mobile-first users — expects fast, smooth mobile browsing
- Comfortable with Arabic interfaces; familiar with English product terminology
- Highly familiar with WhatsApp as a communication and commerce tool

### 3.2 Store Admin

- The 2X Store owner — single admin user
- Needs to manage products, inventory, offers, and incoming orders with minimal technical knowledge
- Requires a simple, Arabic-friendly admin panel

---

## 4. Design & Brand Direction

### 4.1 Visual Identity

The 2X Store logo is black with bold typography. The visual design blends three aesthetics:

- **Dark & Bold** — black/dark backgrounds, strong contrast, dominant typography *(primary aesthetic)*
- **Clean & Minimal** — purposeful white space, structured layout, uncluttered product display
- **Energetic & Colorful** — strategic color accents on CTAs, offer badges, sale highlights, and hover states

### 4.2 Language & Localization

- UI language: **Arabic** (RTL layout — right-to-left)
- Product names, colors, sizes, prices, and numbers: **English**
- Navigation, page titles, buttons, labels, error messages: **Arabic**
- No language toggle — Arabic-first is the only mode
- Currency: **Egyptian Pound (EGP)**

### 4.3 Responsive Design

- Mobile-first design — optimized for phones (primary device of target audience)
- Fully responsive on tablet and desktop
- RTL (right-to-left) layout throughout

---

## 5. Site Structure & Pages

| Page | Route | Description |
|---|---|---|
| Home | `/` | Hero, featured products, offers/sale banners, categories |
| Products (Catalog) | `/products` | Full catalog with Category & Style filters |
| Product Detail | `/products/:id` | Images, variants, add to cart, reviews |
| Cart | `/cart` | Cart summary, delivery info, WhatsApp checkout button |
| Login / Register | `/auth` | Email/password, phone OTP, Google login |
| User Profile | `/profile` | Name, phone, saved addresses, order history |
| Admin — Dashboard | `/admin` | Overview stats, quick actions |
| Admin — Products | `/admin/products` | Add / edit / delete products |
| Admin — Inventory | `/admin/inventory` | Stock per variant (size × color) |
| Admin — Offers | `/admin/offers` | Create sale prices, promo banners |

---

## 6. Feature Specifications

### 6.1 Home Page

- Hero banner with promotional image/text and a primary CTA button
- Offers & sale section — highlights discounted products with percentage badges
- Featured products row — hand-picked by admin
- Category quick-links (T-Shirts, Pants, Jackets, etc.)
- Style quick-links (Streetwear, Casual, Formal)
- Fully responsive, visually bold layout

### 6.2 Product Catalog Page

- Grid display of all products (2 columns on mobile, 3–4 on desktop)
- Filter by **Category** (T-Shirts, Pants, Jackets, Shoes, Accessories, etc.)
- Filter by **Style** (Streetwear, Casual, Formal)
- Sale/Offer badge displayed on discounted product cards
- Out-of-stock products shown with a clear unavailable state
- No search bar, no price filter, no size/color filter — keep it simple at launch

### 6.3 Product Detail Page

- Multiple product images (gallery/carousel)
- Product name (English), description (Arabic), price in EGP
- Color selector — visual swatches
- Size selector (S, M, L, XL) — sold-out sizes are greyed out automatically
- Quantity selector
- "Add to Cart" button — works for both guests and logged-in users
- Original price + sale price displayed when a discount is active
- Product reviews & ratings section (star rating + written review)
- Only verified buyers can leave reviews (linked to WhatsApp order history)

### 6.4 Cart & WhatsApp Checkout

This is the core conversion flow. When the customer is ready to order:

- Cart shows all selected items: product name, color, size, quantity, unit price, subtotal
- Total order price displayed prominently in EGP
- Customer fills in their name
- Customer chooses delivery method: **type address manually** OR **drop a Google Maps location pin**
  - If typed address: full address text field
  - If location pin: Google Maps location picker — the URL/coordinates are captured
- A confirmation prompt: *"Is this your correct delivery location?"* before proceeding
- On confirm: a pre-filled WhatsApp message is generated and the customer is redirected to the owner's WhatsApp

**WhatsApp Message Format:**

The message will include:
- Greeting in Arabic
- Customer name
- Each product: name / color / size / quantity / unit price
- Total order price in EGP
- Delivery address (typed) or Google Maps location link

**Cart rules:**
- Guest users: can complete checkout without an account
- Registered users: name and saved address are pre-filled automatically

### 6.5 User Authentication & Accounts

- Registration: email + password, OR phone number with OTP verification
- Login: email/password, phone/OTP, or Google Sign-In (OAuth)
- Phone OTP is required on first registration to ensure real users
- Google login for frictionless sign-up
- Password reset via email

### 6.6 User Profile

- Full name and phone number
- Saved delivery addresses (typed) and saved location pins (Google Maps)
- Saved cart — registered users can save cart and return to it later
- Order history — log of all orders sent to WhatsApp (product details, date, total price)
- Guest users lose their cart on session end; registered users retain it

### 6.7 Product Reviews & Ratings

- Star rating (1–5) and optional written review per product
- Only users who have placed an order for that product can leave a review
- Reviews show: reviewer name, rating, date, review text
- Average rating displayed on product card and product detail page
- Admin can delete inappropriate reviews

### 6.8 Admin Panel

#### Product Management
- Add new product: name (English), description (Arabic), category, style, images (multiple), base price
- Add variants: each combination of color + size gets its own stock quantity and optional variant-level price
- Edit any product field or variant
- Delete product (soft delete — keeps order history intact)
- Upload multiple product images; set a primary/cover image

#### Inventory Management
- View stock levels per product variant (size × color matrix)
- Update stock quantity per variant
- When a variant's stock reaches 0: automatically shown as sold-out on the storefront
- Low-stock alert in admin panel (configurable threshold)

#### Offers & Discounts
- Set a sale price on any product (original price shown with strikethrough on storefront)
- Set offer start and end dates (auto-activates and expires)
- Create homepage promo banners: image, text, CTA button, linked URL
- Mark products as "Featured" to appear on the homepage featured row
- Offer badge automatically appears on product cards and detail pages

---

## 7. WhatsApp Checkout Flow — Detailed

| Step | User Action | System Behavior |
|---|---|---|
| 1 | Browses catalog, opens product page | Page loads with all variants |
| 2 | Selects color, size, quantity | Add to Cart button activates; sold-out combos blocked |
| 3 | Clicks "Add to Cart" | Item added; cart icon updates with count |
| 4 | Continues shopping or opens cart | Cart displays all items with totals |
| 5 | Clicks "Order via WhatsApp" | Checkout form appears |
| 6 | Enters name; chooses address or location pin | Address typed OR Maps picker opens |
| 7 | Confirms delivery location | Confirmation dialog shown |
| 8 | Clicks "Send Order" | WhatsApp opens with pre-filled order message |
| 9 | Sends message on WhatsApp | Owner receives order; cart cleared; order saved to history |

---

## 8. Core Data Models

### Product

| Field | Type | Notes |
|---|---|---|
| id | UUID | Primary key |
| name_en | String | Product name in English |
| description_ar | Text | Product description in Arabic |
| category | Enum | T-Shirt, Pants, Jacket, Shoes, Accessories, etc. |
| style | Enum | Streetwear, Casual, Formal |
| base_price | Decimal | Price in EGP |
| sale_price | Decimal / null | Null if no active offer |
| sale_start / sale_end | DateTime / null | Offer validity window |
| is_featured | Boolean | Show on homepage |
| images | Array\<String\> | Image URLs; first = cover |
| is_deleted | Boolean | Soft delete flag |

### Product Variant

| Field | Type | Notes |
|---|---|---|
| id | UUID | Primary key |
| product_id | UUID | Foreign key → Product |
| color | String | e.g. Black, White, Navy |
| size | Enum | S, M, L, XL |
| stock_qty | Integer | Current stock level |
| variant_price | Decimal / null | Override base price if needed |

### User

| Field | Type | Notes |
|---|---|---|
| id | UUID | Primary key |
| name | String | Full name |
| email | String / null | Optional if phone-only registration |
| phone | String | Egyptian phone number |
| auth_method | Enum | email_password, phone_otp, google |
| saved_addresses | Array\<Object\> | Label + address text or Maps URL |
| saved_cart | JSON / null | Persisted cart items |
| role | Enum | customer, admin |

### Order (WhatsApp Log)

| Field | Type | Notes |
|---|---|---|
| id | UUID | Primary key |
| user_id | UUID / null | Null for guest orders |
| items | JSON | Array of product/variant/qty/price snapshots |
| total_price | Decimal | Total in EGP at time of order |
| delivery_address | String / null | Typed address |
| delivery_location_url | String / null | Google Maps link |
| customer_name | String | Name entered at checkout |
| customer_phone | String | Phone at checkout |
| whatsapp_sent_at | DateTime | Timestamp of WhatsApp redirect |

---

## 9. Non-Functional Requirements

| Requirement | Specification |
|---|---|
| Performance | Page load < 2s on 4G mobile; image lazy loading; CDN for media |
| Scalability | Stateless backend; horizontal scaling ready; modular architecture for Phase 2 features |
| Security | HTTPS everywhere; JWT auth; input validation; admin routes protected |
| SEO | Server-side rendering or static generation for product pages; Arabic meta tags |
| Accessibility | RTL support; sufficient color contrast; touch-friendly tap targets (min 44px) |
| Uptime | 99.5% target; cloud hosting with automatic failover |
| Image Handling | Compressed WebP format; max 500KB per image; 1:1 and 4:3 aspect ratio support |

---

## 10. Recommended Tech Stack

| Layer | Technology | Reason |
|---|---|---|
| Frontend | Next.js (React) | SSR/SSG for SEO, RTL support, fast performance |
| Styling | Tailwind CSS | Rapid styling, dark mode, RTL utilities |
| Backend | Node.js + Express or Next.js API routes | JavaScript full-stack, easy scaling |
| Database | PostgreSQL | Relational, strong for inventory/variants/orders |
| Auth | NextAuth.js | Supports email, Google OAuth, easy to extend |
| OTP | Twilio / Africa's Talking | Egyptian phone number OTP support |
| Image Storage | Cloudinary or AWS S3 | CDN delivery, compression, transformation |
| Hosting | Vercel (frontend) + Railway/Supabase (backend/DB) | Easy deployment, scalable |
| WhatsApp | wa.me deep link | No API needed — native WhatsApp redirect |

---

## 11. Phase 2 Roadmap

| Feature | Description | Impact |
|---|---|---|
| Real Payment Gateway | Integrate Paymob or Fawry for in-app card/wallet payments | Full e-commerce conversion |
| Order Tracking | Admin dashboard to manage order statuses (pending → shipped → delivered) | Operational efficiency |
| Push Notifications | Browser and mobile push for new arrivals, offers, order updates | Retention & re-engagement |
| Mobile App | iOS & Android app using React Native (shared codebase with web) | Broader reach |
| Loyalty Program | Points per purchase, redeemable discounts | Customer retention |

---

## 12. Out of Scope — Phase 1

- Payment gateway (Paymob, Fawry, credit card processing)
- Order tracking / status management in admin panel
- Push notifications
- Mobile app (iOS / Android)
- Multi-language toggle (English UI)
- Price range filter, size filter, color filter on catalog page
- Multiple admin users or role-based permissions
- Marketplace / multi-seller functionality
- Loyalty or rewards program
- Live chat (other than WhatsApp redirect)

---

## 13. Open Questions & Decisions Needed

| # | Question | Owner |
|---|---|---|
| 1 | What product categories should be included at launch? (e.g. T-Shirts, Pants, Jackets, Shoes, Accessories) | Store Owner |
| 2 | What is the owner's WhatsApp business number for order redirects? | Store Owner |
| 3 | What are the initial offer/promo campaigns for homepage banners at launch? | Store Owner |
| 4 | What is the low-stock alert threshold in the admin panel? (e.g. < 5 units) | Store Owner |
| 5 | Should the admin panel be in Arabic or English? | Store Owner |
| 6 | Which hosting provider does the owner prefer? | Dev Team |
| 7 | What is the OTP provider for Egyptian phone verification? (Twilio vs local provider) | Dev Team |

---

*2X Store PRD v1.0 — Confidential*
>>>>>>> 96b462cb9dc8d97c0a18a9cc04aa1ac8db06d80a
