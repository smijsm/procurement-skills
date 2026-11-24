# Transport rules, carriers and costs

Part of the skill `dangerous-goods-pre-order-check`. Read this file when the product is confirmed or likely dangerous goods and one of these is true: the buyer books the transport, the goods cross a border as freight, the goods travel by sea or air, or the user asks about packaging, papers, carriers or costs.

The facts were checked in November 2026. ADR and RID get a new edition on 1 January of every odd year, IMDG amendments become mandatory on 1 January of every even year, and the IATA rules change every 1 January.

## Contents

- Road and rail rules
- Delivery terms
- Chemicals, by transport mode
- Lithium batteries
- Imports into the United States
- Carrier and ports
- Costs and deadlines
- Requests to the supplier

## Road and rail rules

ADR and RID apply when both countries apply ADR. Otherwise national rules apply, such as 49 CFR in the US and TDG in Canada.

Countries that apply ADR: AL AD AM AT AZ BY BE BA BG HR CY CZ DK EE FI FR GE DE GR HU IS IE IT KZ LV LI LT LU MT MD ME MA NL NG MK NO PL PT RO RU SM RS SK SI ES SE CH TJ TN TR UG UA GB UZ.

## Delivery terms (Incoterms 2020)

| Term | Books the main transport | Clears import |
|---|---|---|
| EXW, FCA | Buyer | Buyer |
| FAS, FOB (sea only) | Buyer | Buyer |
| CFR, CIF (sea only) | Supplier | Buyer |
| CPT, CIP, DAP, DPU | Supplier | Buyer |
| DDP | Supplier | Supplier |

Catalog orders inside one country or inside the EU usually arrive at the door with the supplier's carrier. Treat them as "supplier books the transport" unless the order says otherwise.

## Chemicals, by transport mode

- Limited quantities (all modes except air): if each inner pack is at or under the limit for the UN number, the shipment travels with far fewer formalities. A box weighs up to 30 kg and shows the limited-quantity mark. If the limit or the pack size is unknown, ask for both.
- Road and rail, limited quantities: no dangerous goods transport document on ADR routes. Elsewhere this depends on national rules.
- Road and rail, above the limit: fully regulated. The supplier needs UN-approved packaging, hazard labels and a transport document with UN number, class and packing group. The carrier must be set up for the class. Above small-load thresholds the driver needs dangerous goods training and the vehicle orange plates. Give the carrier class and quantity with the quote request.
- Road and rail outside ADR: ask the carrier or forwarder which rules apply on each leg.
- Sea: a dangerous goods declaration (IMDG) is required even for small packs. Whoever loads the container signs a container packing certificate. Limited quantities lighten the packaging rules and are stated on the declaration. Above the limit, the goods need tested packaging with a UN mark and hazard labels. A marine pollutant must be declared and marked.
- Air: a Shipper's Declaration for Dangerous Goods, signed by trained staff. The air rules set a maximum per package for every UN number, separately for passenger and cargo aircraft, and some goods may not fly. Have the forwarder confirm it for the pack size.

## Lithium batteries

- Always get the UN 38.3 test summary. Carriers ask for it.
- Get the watt-hours per battery (lithium-ion) or the lithium content (lithium-metal). 100 Wh or 2 g is the line between the simplified and the fully regulated rule.
- Road, rail and sea, at or under the line: the small-battery rule (special provision 188) applies. Tested type, strong outer box, lithium battery mark, boxes up to 30 kg, and a built-in battery protected against switching on. No dangerous goods transport document.
- Road, rail and sea, above the line: fully regulated class 9 with UN-approved packaging, the class 9 battery label and a transport document.
- Sea: carriers ask for battery details, data sheet and test summary at booking, even under the simplified rule.
- Air, batteries alone: cargo aircraft only, with a shipper's declaration. Lithium-ion batteries ship at 30% charge or less.
- Air, batteries packed with a device: lithium-ion batteries over 2.7 Wh ship at 30% charge or less. This is mandatory since January 2026.
- Air, in or with a device, at or under the line: no shipper's declaration. The box carries the lithium battery mark where required. Above the line: fully regulated with a shipper's declaration.

## Imports into the United States

Imports into the United States, except from Canada: the importer must give the foreign shipper and the forwarder at the port of entry written information on the US hazardous materials rules that apply. Unless the goods ship as limited quantities, the shipping papers need an emergency phone number that is answered at any time during transport.

## Carrier and ports

When the supplier delivers inside one country or inside the EU, reduce this group to one note: dangerous goods often cannot use express or next-day services, so check the delivery time if the date matters. Use the full group when the buyer books the transport or the route is an import.

- No delivery term agreed: agree one. The Incoterm decides who books the transport, who pays the dangerous goods surcharges and who clears customs.
- EXW with dangerous goods: avoid it. EXW leaves loading and export clearance to the buyer. Under FCA the supplier loads and clears export.
- FAS, FOB, CFR or CIF for road, rail or air: pick a term that fits, such as FCA, CPT, CIP, DAP or DDP.
- Carrier acceptance: whoever books the transport gets the carrier's written acceptance of the UN number and class before the order is firm. If the supplier books, ask the supplier to confirm it.
- Sea: ask for the dangerous goods cut-off. The final declaration is due 2 to 3 working days before the ship, and late papers move the container to the next sailing. Ask for the full routing, because every port where the container changes ship has its own restrictions. Ask which export approvals the loading port needs. Plan the pick-up at the arrival port before the ship arrives: hazardous containers get fewer free days and higher daily rates.
- Air: ask which airline flies it and where it stops. Airlines and countries add their own restrictions. The airline checks every package and paper at hand-over and refuses the shipment on a single error.
- Parcel and express: these services take dangerous goods only from approved shippers under contract, and not every class. Check that an account exists.

## Costs and deadlines

Add this block only when something applies. The prices are examples from 2025 and 2026 price lists. Say so, and tell the reader to ask for a quote.

- Sea, carrier surcharge: about 200 USD per container for most classes, 300 for lithium batteries and class 4, 325 to 500 for class 5, and far more for a few entries.
- Sea, waiting in port (Hamburg example): 1 free day, then 95 EUR a day for a hazardous 20-foot container. Normal cargo gets 3 free days, then 70 EUR a day.
- Sea, wrong declaration: carriers charge up to 15,000 USD per container for misdeclared dangerous goods.
- Parcel and express: about 25 EUR per shipment for limited quantities, about 100 EUR for fully regulated goods, about 5 EUR for small batteries packed with a device.
- Air, road and rail freight: the carrier charges a dangerous goods fee per shipment. Ask for it with the quote.
- Deadlines: take them from `customs-and-country-rules.md`.

## Requests to the supplier

Usual requests for the message to the supplier: the current safety data sheet; whether the product is dangerous goods for transport (section 14); UN number, class and packing group; the limited-quantity limit and the size of the inner packs; confirmation that it ships as limited quantities; a draft dangerous goods declaration (sea) or Shipper's Declaration (air); written confirmation that the carrier accepted the goods; the customs tariff code and the country of origin; a proof of origin; the importer of record under DDP; a safety data sheet for the destination country in its language; a statement that no ingredient is banned or restricted there; for batteries the UN 38.3 test summary and the watt-hours per battery.
