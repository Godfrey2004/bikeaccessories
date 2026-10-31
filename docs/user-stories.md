
# RIDEFORGE — User Stories and Acceptance Criteria

## US-01: Browse Products

**Priority:** Must have

**User Story:**
As a customer, I want to browse motorcycle accessories
so that I can discover products available at the shop.

**Acceptance Criteria:**
- The product listing displays available products.
- Each product shows its name, image and price.
- Selecting a product opens its detail page.
- If no products are available, a suitable message is displayed.

## US-02: Search Products

**Priority:** Should have

**User Story:**
As a customer, I want to search products by name
so that I can find an accessory quickly.

**Acceptance Criteria:**
- A customer can enter a search term.
- Matching products are displayed.
- Search is case-insensitive.
- An empty result displays a clear message.
- Clearing the search restores the full listing.

## US-03: Manage Products

**Priority:** Must have

**User Story:**
As an administrator, I want to create and update products
so that the catalogue remains accurate.

**Acceptance Criteria:**
- Only authorized administrators can modify products.
- Required fields are validated.
- Invalid prices are rejected.
- Successfully saved changes appear in the catalogue.

## US-04: Create an Invoice

**Priority:** Must have

**User Story:**
As billing staff, I want to select products and quantities
so that I can generate a customer invoice.

**Acceptance Criteria:**
- Staff can search and select products.
- Staff can enter valid quantities.
- The system calculates the subtotal.
- Tax and discount calculations follow approved business rules.
- A finalized invoice is saved and can be printed.

## US-05: Update Inventory

**Priority:** Must have

**User Story:**
As a shop owner, I want finalized bills to update stock
so that inventory reflects completed sales.

**Acceptance Criteria:**
- Finalization deducts the correct quantities.
- Insufficient stock is handled according to shop policy.
- Failed operations do not leave partial inventory updates.
- Retrying finalization does not deduct stock twice.

## Open Questions
- Which tax and invoice rules apply?
- Can billing staff approve discounts?
- How should returns and cancellations affect inventory?
