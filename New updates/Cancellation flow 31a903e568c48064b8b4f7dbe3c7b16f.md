# Cancellation flow

Created: March 5, 2026 1:05 PM
Files & media: ../Screenshot_2026-03-05_at_14.27.10.png

A cancellation flow triggers when a subscriber **attempts to cancel their subscription**. Building this in Juo helps you achieve two primary goals:

- Understand cancellation reasons.
- Convince subscribers to stay by:
    - Explaining the value of your product.
    - Highlighting the perks of being a subscriber.
    - Addressing their specific needs.

### ⚙️ Workflow Setup

**Trigger:** Subscription cancellation requested

- **Show content:** Display images and videos explaining the value of your brand.
- **Poll:** Learn the exact reason for canceling.
- **Offer alternatives:** Depending on the poll response, offer a discount, free product, product swap, frequency change, or skip option as an alternative to canceling.

### 💡 Best practices

#### Explain the value of your product and subscription

Before tempting your subscribers with discounts and free products, make sure they understand the value of your subscription and the benefits of building a habit. This is what ultimately makes them stick around and keeps your product as a part of their routine. Freebies can be effective, but consider them a last resort rather than the core of your retention strategy.

#### Personalize for new and long-term subscribers

Your loyal subscribers have different reasons for canceling than people who subscribed just a few days (or hours!) ago.

There’s no point in asking fresh subscribers if they have stocked up too much. Instead, it might be a better idea to explain the long-term value to them, or show them how to use the product — content that wouldn't be very useful to someone who has already been subscribed for a year.

Useful conditions:

- `subscription.cycle_count`
- `subscription.age_days`

#### Personalize depending on the subscribed product

You can create tailored routes for people subscribed to a specific product. Maybe it’s your flagship subscription-first product, or maybe it’s a brand-new release that you’d like to get targeted feedback on.

Use the condition below in the workflow to check for a specific product variant:

- `subscription.items contains item where variantId is equal to`

![image.png](Cancellation%20flow/image.png)