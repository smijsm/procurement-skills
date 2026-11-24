# Example results

Part of the skill `dangerous-goods-pre-order-check`. Two full results that show the expected length and tone.

**Example 1: product check, domestic.** The user found "Brake cleaner spray 500 ml" and wants 48 cans for a workshop in Munich. The system gives the name and a supplier in Germany. It has no hazard data.

```
**Brake cleaner spray 500 ml, 48 cans: within Germany, delivered by the supplier**
Likely dangerous goods (spray can, typically UN 1950). Nothing blocks the order. Two points are open.

Based on: product name and supplier country from the system. Delivery by road is assumed. The catalog has no hazard data.

**Product and transport rules**
- Supplier: send the safety data sheet. Section 14 confirms the UN number, and your site needs the sheet anyway.
- Supplier: confirm that the cans ship as limited quantities. Cans up to 1 L in boxes up to 30 kg travel with the limited-quantity mark and without a dangerous goods transport document.

**At your site**
- You: check storage for 48 cans, which is 24 L of flammable aerosol. Section 7 of the safety data sheet gives the limits.
- You: if the product is new to the site, add it to the list of hazardous products and brief the users.

**Not needed here:** customs and importer duties (the goods stay in Germany). Carrier acceptance (the supplier ships).

This is a checklist to verify, not legal advice. Built-in facts are from November 2026.
Do you want a short message to the supplier with the two requests?
```

**Example 2: approval review.** The user asks whether order 4711 can be approved. It has five lines from one supplier in the same country.

```
**Order 4711: Supplier A, 5 lines, delivery to Lyon, France**
**Verdict: Open points.** Two lines are likely dangerous goods and the system holds no safety data sheet for them.

| Line | Product and quantity | Finding | Before approval |
|---|---|---|---|
| 2 | Two-component epoxy adhesive, 12 kits | Likely hazardous, possibly dangerous goods. No hazard data in the system. | Ask for the safety data sheet. Check whether users need protective equipment. |
| 4 | Cordless drill with 2 batteries 18 V 5 Ah, 6 sets | Lithium-ion batteries of 90 Wh each, packed with the device. Under the 100 Wh line. | Nothing for transport. Check where the batteries are charged and stored. |

Lines without signs: 1, 3, 5.
**Ask the requester:** Was the adhesive bought before? Who will use it?
**Suggested approval comment:** Approved on condition that the safety data sheet for the epoxy adhesive (line 2) is on file before first use and that storage and charging of the batteries (line 4) follow the site's fire rules.

This is a checklist to verify, not legal advice. Built-in facts are from November 2026.
```
