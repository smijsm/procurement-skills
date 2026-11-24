# procurement-skills

Skills that help buyers and approvers check things before they buy.

A skill is a plain text file (`SKILL.md`) that an AI assistant loads when a task calls for it. The skills here are vendor-neutral. They do not depend on a specific procurement system. They work with any system that is connected to the assistant through an MCP server (Model Context Protocol), and they also work when the user pastes the details by hand.

## Skills

| Skill | What it does |
|---|---|
| [dangerous-goods-pre-order-check](dangerous-goods-pre-order-check/) | Checks what must be settled before a hazardous product is ordered: transport rules, carrier acceptance, customs, rules in the destination country and what the site needs. Works for a product someone found and for an order that waits for approval. |

## Install

Every skill folder holds two files:

- `SKILL.md`: the skill as readable text.
- `<skill-name>.skill`: the same skill as a package you can upload.

The README in the skill folder has the steps.

## Please note

These skills produce checklists to verify. They are not legal advice. Rules for dangerous goods, customs and chemicals change often, and each skill states the date its facts were checked. Confirm anything that decides an order with the supplier, the carrier, a customs broker or a dangerous goods adviser.

## License

MIT. See [LICENSE](LICENSE).
