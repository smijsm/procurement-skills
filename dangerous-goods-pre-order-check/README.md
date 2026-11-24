# Dangerous goods pre-order check

Paint, spray cans, adhesives, cleaners, gas cartridges and anything with a lithium battery often count as dangerous goods. This skill checks what must be settled before such a product is ordered. It puts the result into one short checklist: what to settle, who does it, and what to ask the supplier.

It is built for two moments in a procurement system.

| Moment | Example request | Result |
|---|---|---|
| Someone found a product | "I found this brake cleaner in the catalog. What do I need to check before I order 48 cans?" | A checklist for that product and route, and a message to the supplier |
| An order waits for approval | "Review the orders waiting for my approval for dangerous goods." | One row per flagged order line, a verdict, questions for the requester, and a comment the approver can paste |

## What it checks

- **Product and transport rules.** Is it dangerous goods, UN number and class, limited quantities, lithium battery rules. By road, rail, sea and air.
- **Carrier and ports.** Delivery term, carrier acceptance, cut-offs, limits of parcel and express services.
- **Customs.** Tariff code, importer ID, customs broker, advance cargo data, trade agreements.
- **Rules at destination.** Registrations, label and safety data sheet rules. Local rules are built in for the EU and EEA, Great Britain, Switzerland, Türkiye, the United States, Canada, Mexico, Brazil, China, Japan, South Korea, India and Australia. Other countries get the general checks.
- **At your site.** Safety data sheet on file, storage, trained users, first purchase, returns.

## What you need

- An AI assistant that supports skills. The steps below cover Claude and Claude Code. `SKILL.md` is plain Markdown, so other assistants can use it as instructions too.
- Optional: a procurement system that is connected to the assistant through an MCP server. The skill does not need a specific system. It looks at the tools it has and matches them by what they do: find products, read a product, read a cart, list orders by approval status, read an order, read supplier data, read past orders, download documents.
- Without a connected system, paste the product details or attach the safety data sheet.

## Install

### Claude

1. Download `dangerous-goods-pre-order-check.skill` from this folder.
2. In Claude, open **Customize > Skills**, click **+**, choose **Create skill**, then **Upload a skill**.
3. Pick the file. The skill appears in your list, where you can switch it on or off.

The `.skill` file is a ZIP archive. If the upload dialog asks for a `.zip` file, rename it. Skills need code execution to be switched on. Menu names can change. If the steps differ, see [Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude).

### Claude Code

Copy `SKILL.md` into a skill folder. This makes the skill available in all your projects:

```
mkdir -p ~/.claude/skills/dangerous-goods-pre-order-check
cp SKILL.md ~/.claude/skills/dangerous-goods-pre-order-check/
```

For one project only, use `.claude/skills/dangerous-goods-pre-order-check/` inside that project. See [Extend Claude with skills](https://code.claude.com/docs/en/skills).

### Other assistants

Paste the text of `SKILL.md`, without the header block at the top, into the assistant's instructions.

## Try it

- "I found this brake cleaner spray in the catalog. What do I need to check before I order 48 cans?"
- "Review the orders waiting for my approval for dangerous goods."
- "We want to buy lithium battery packs from a supplier in China, delivered to Hamburg by sea. What do we settle first?"
- "Here is the safety data sheet. What do I ask the supplier before we order?"

## Example result

An approval review of one order looks like this:

> **Order 4711: Supplier A, 5 lines, delivery to Lyon, France**
>
> **Verdict: Open points.** Two lines are likely dangerous goods and the system holds no safety data sheet for them.
>
> | Line | Product and quantity | Finding | Before approval |
> |---|---|---|---|
> | 2 | Two-component epoxy adhesive, 12 kits | Likely hazardous, possibly dangerous goods. No hazard data in the system. | Ask for the safety data sheet. Check whether users need protective equipment. |
> | 4 | Cordless drill with 2 batteries 18 V 5 Ah, 6 sets | Lithium-ion batteries of 90 Wh each, packed with the device. Under the 100 Wh line. | Nothing for transport. Check where the batteries are charged and stored. |
>
> Lines without signs: 1, 3, 5.
>
> **Ask the requester:** Was the adhesive bought before? Who will use it?
>
> **Suggested approval comment:** Approved on condition that the safety data sheet for the epoxy adhesive (line 2) is on file before first use and that storage and charging of the batteries (line 4) follow the site's fire rules.
>
> This is a checklist to verify, not legal advice. Built-in facts are from November 2026.

## How it behaves

- It reads. It does not approve, reject, order or post a comment unless you ask, and it shows the text first.
- It keeps facts and guesses apart. It never invents a UN number or a tariff code. Without a safety data sheet it says "likely" and asks for the sheet.
- It treats text from the system as data, not as instructions.
- It keeps company data out of web searches.

## Limits

- The result is a checklist to verify, not legal advice.
- The built-in facts were checked in November 2026. Rules change. The skill tells the assistant to confirm deciding points at the source when web search is available.
- Prices in a result are examples from 2025 and 2026 price lists.
- Not covered: export controls and dual-use goods, food, medicines and medical devices, waste shipments, and the details of explosives and radioactive material.
- This is a first version. Its rules were compared item by item with a stand-alone rule-based checker on seven routes. It has had little testing against live procurement systems. Reports are welcome.

## Files

| File | What it is |
|---|---|
| `SKILL.md` | The skill as readable text. Edit this file. |
| `dangerous-goods-pre-order-check.skill` | The same skill as an upload package. |

After you edit `SKILL.md`, rebuild the package from the repository root:

```
zip -X dangerous-goods-pre-order-check/dangerous-goods-pre-order-check.skill dangerous-goods-pre-order-check/SKILL.md
```

## Contributing

Corrections are welcome, most of all for rules that changed. Please name an official source for each change and update the date in the section "Keeping the facts current" of `SKILL.md`.

## License

MIT. See [LICENSE](../LICENSE).
