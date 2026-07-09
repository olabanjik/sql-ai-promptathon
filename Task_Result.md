# Task 1 Result

## Summary
Based on the SQL analysis of the PromptathonDb database, the strongest sales-impact candidates are:

- Category-level:
  - B2B: $969,792.32 revenue, 1,989 units, 12 orders
  - Elite: $277,368.69 revenue, 3,222 units, 1,273 orders
  - Premium: $190,553.87 revenue, 2,207 units, 893 orders

- Product-level:
  - ZavaCore Systems Professional Athletic Jersey (B2B): $521,612.54 revenue, 1,332 units, 9 orders
  - ZavaCore Smart Cleat (B2B): $448,179.78 revenue, 657 units, 6 orders
  - Premium Short Sleeve Men’s Top: $19,825.05 revenue, 228 units, 105 orders
  - Elite Long Sleeve Men’s Top: $19,149.86 revenue, 222 units, 112 orders

## Takeaway
- B2B products drive the largest revenue concentration.
- Elite and Premium products show the highest unit volume and broad customer reach.
- For the next step in the mission, the most relevant products to investigate are the B2B jersey and cleat lines, alongside the high-volume Elite and Premium tops.

# Task 2 Result

## Understanding of Task 2
Task 2 is the support-side comparison step: it compares the high-sales products and categories from Task 1 against support ticket volume, priority, status, and customer satisfaction to find whether the biggest sellers also carry an outsized support burden and weaker customer experience.

## Key Finding
The strongest support-risk signal is the Premium Short Sleeve Men’s Top.

- It generated 9 support tickets, the highest ticket count among the directly comparable product-level results.
- Its average satisfaction score was 1.67, which is materially lower than the Elite category average of 3.71 and lower than other comparable premium items.
- The ticket mix included 1 critical, 2 high, 3 medium, and 3 low-priority cases.
- Status distribution was 3 resolved and 6 closed, with no open tickets at the time of the query.

## Category-Level Comparison
- Premium category: 19 tickets, average satisfaction 2.79, 2 critical, 2 high, 0 open, 9 resolved
- Elite category: 14 tickets, average satisfaction 3.71, 1 critical, 4 high, 0 open, 6 resolved

## Conclusion
The Premium Short Sleeve Men’s Top stands out because it combines meaningful sales volume with unusually high support burden and weak satisfaction, making it the strongest candidate for the next phase of the mission.

# Task 3 Result

## Understanding of Task 3
Task 3 is the qualitative analysis step: it uses the support chat transcripts to identify recurring complaint themes that explain why customers are contacting support about the product.

## Recurring Complaint Themes
The chat transcripts for the Premium Short Sleeve Men’s Top show a small set of recurring issues:

- App and connectivity friction: customers asked whether the product needed a special app and reported that it would not stay connected to the app.
- Billing and renewal confusion: one customer did not recognize a $19.99 charge and believed the product was already covered.
- Returns and product fit expectations: customers asked to start returns because the product did not meet their needs or expectations.

## Representative Excerpts
- “Does it need a special app to work?”
- “The fabric doesn’t connect to the application anymore.”
- “I need help with a charge… I thought my product was already covered.”
- “I want to return my product… it doesn’t meet what I needed.”

## Interpretation
These themes suggest that the main pain points are not isolated shipping or order issues, but product usability, app experience, and post-purchase billing/return friction.

# Task 4 Result

## Understanding of Task 4
Task 4 is the document-analysis step: it uses the Docs table to look for negative reviews and support-chat documents that reinforce the complaint themes seen in tickets and chat transcripts.

## Negative Document Evidence
The Docs table contains multiple negative records linked to the Premium Short Sleeve Men’s Top and the broader Zava smart fabric product experience.

- Review documents: 6 relevant review records
- Support-chat documents: 28 relevant support-chat records
- The strongest negative review themes are:
  - smart fabric stops connecting after washing
  - app loses the sensor after laundry
  - premium product fails quickly after a few washes
  - conductive thread does not survive normal care

## Representative Negative Excerpts
- “After the very first wash it stopped pairing with the Zava app entirely.”
- “The app shows the sensor as offline and re-pairing never works.”
- “This top loses its connection to the companion app every time I wash it.”
- “The garment is comfortable but the connected features, which are the whole point, are dead.”

## Conclusion
The document evidence strongly supports the earlier ticket and chat findings: the core issue is product durability and connectivity, especially after washing, rather than simple shipping or order fulfillment problems.

# Task 5 Result

## Understanding of Task 5
Task 5 uses the vector similarity tool to confirm whether negative documents cluster around the same product or issue pattern rather than being isolated complaints.

## Representative Negative Document
I used the review document with DocId 39 as the seed for similarity search because it clearly describes a wash-related connectivity failure for the Premium Short Sleeve Men’s Top.

## Similarity Search Findings
The similarity search returned a tight cluster of related documents around the same SKU, ZCPTM-SS-M-BW.

- The exact match was the original document itself.
- The nearest related documents were other reviews about:
  - connectivity failing after washing,
  - app losing the sensor after laundry,
  - broken smart features after repeated wash cycles.
- The closest matches all pointed to the same SKU and the same issue pattern: smart-fabric connectivity failure after washing.

## Cluster Interpretation
The similar complaints cluster around the same product and the same root issue rather than spreading across unrelated products or categories. That strengthens the case that the problem is product-specific and quality-related.

# Task 6 Result

## Understanding of Task 6
Task 6 determines how the complaints cluster across the business dimensions that matter for intervention, including SKU, product category, order type, channel, customer segment, country, and language.

## Cluster Summary
The strongest complaint cluster is concentrated around the Premium Short Sleeve Men’s Top (SKU ZCPTM-SS-M-BW), in the Premium category, and it appears in B2C orders.

### By product and category
- All of the closest negative documents are tied to the same SKU: ZCPTM-SS-M-BW.
- The product name and category are consistent across the cluster: Premium Short Sleeve Men’s Top / Premium.

### By order type and channel
- The cluster is concentrated in B2C orders.
- The order channels are primarily Online and Retail-SanFrancisco / Retail-London, with one additional online case.

### By customer segment and geography
- The related customers are mostly labeled as New customers.
- The countries represented include Canada, France, Germany, Poland, and Russia.
- The languages represented include French, German, Polish, and Belarusian, which suggests the issue is not limited to one locale.

## Conclusion
The complaints cluster around a single premium B2C product with a recurring wash-related connectivity failure, and the pattern appears across multiple countries and languages rather than being isolated to one customer segment or channel.

# Task 7 Result

## Recommendation
Prioritize an urgent product-quality and support-response intervention for the Premium Short Sleeve Men’s Top (SKU ZCPTM-SS-M-BW).

## Rationale
This recommendation is supported by the evidence from Tasks 1 through 6:

- The product combines meaningful sales impact with a high support burden.
- It has the strongest documented support dissatisfaction, with 9 tickets and an average satisfaction score of 1.67.
- The recurring complaint themes are consistent across chats, tickets, and reviews: wash-related connectivity failure, app/sensor disconnection, and confusion around billing and returns.
- The vector similarity search shows that the negative documents cluster tightly around the same SKU and issue pattern.

## Concrete Business Action
Launch a focused containment action for this SKU:

1. Pause or limit further promotion of the Premium Short Sleeve Men’s Top in online and retail channels.
2. Open a product-quality investigation with the manufacturing and engineering teams to inspect the smart-fabric connector and wash durability.
3. Add a proactive support playbook for affected customers, including troubleshooting steps, billing clarification, and return guidance.

## Expected Outcome
If Zava acts quickly, it should reduce repeat support volume, improve customer satisfaction, and prevent further negative reviews from compounding around the same product. The expected result is lower churn risk for a high-value premium SKU and a clearer signal for whether the issue is a design, materials, or manufacturing defect.

# Executive Brief

## 1. Risk cluster
- Product/category: Premium Short Sleeve Men’s Top, Premium category
- Order type and channel: B2C orders, primarily online and retail channels
- Customer segment pattern: mostly New customers, spanning multiple countries and languages

## 2. Evidence
- Revenue and quantity sold: $19,825.05 revenue and 228 units sold for the SKU, with the Premium category showing $190,553.87 revenue and 2,207 units overall
- Support ticket count: 9 tickets for the SKU, with the Premium category showing 19 tickets overall
- Average satisfaction score: 1.67 for the SKU, versus 2.79 for the Premium category and 3.71 for the Elite category
- Priority/status breakdown: 1 critical, 2 high, 3 medium, and 3 low-priority tickets; 3 resolved and 6 closed, with no open tickets in the query snapshot
- Review/support document count: 6 relevant review documents and 28 relevant support-chat documents
- Vector similarity findings: the closest negative documents clustered tightly around the same SKU and the same wash-related connectivity failure pattern

## 3. Complaint themes
- “Does it need a special app to work?”
- “The fabric doesn’t connect to the application anymore.”
- “I need help with a charge… I thought my product was already covered.”
- “I want to return my product… it doesn’t meet what I needed.”

## 4. Recommendation
Zava should launch an urgent containment and quality-investigation effort for the Premium Short Sleeve Men’s Top. The first action should be to pause or limit further promotion of the SKU while engineering and quality teams inspect the smart-fabric connector and wash durability, and support teams deploy a targeted troubleshooting and return playbook.

## 5. Confidence and limitations
Confidence is moderate to high because the findings are consistent across sales, support tickets, support chats, reviews, and vector similarity results. The main limitation is that the dataset is small and the analysis is based on a snapshot of support and document activity rather than a full longitudinal view.
