# Amazon Returns — Claude Cowork Plugin

A Claude Cowork skill plugin that makes Amazon returns fast and hands-off. Tell Claude what to return and where to drop it off — it handles everything else and gets you a QR code.

## What it does

- **Gets you a return QR code** — navigates Amazon, clicks through every screen, and gets you a no-box, no-label QR code for drop-off
- **Handles multiple returns** — say "return my AirPods and the phone case" and it processes them back-to-back
- **Minimal input** — only asks for drop-off location if you didn't say. Never asks unnecessary questions.
- **Always refunds to your original payment method** — never gift card, never Amazon credit
- **Never gets stuck** — uses smart defaults for every intermediate screen so the flow runs end-to-end

## Drop-off locations

- Whole Foods
- UPS Store
- Kohl's
- Staples
- Amazon Fresh

All free, no box, no label needed.

## Install

**From GitHub (recommended):**
```
/plugin marketplace add roccodallas/amazon_returns_skill_for_claude
/plugin install amazon-returns
```

**Or test locally:**
```
claude --plugin-dir /path/to/amazon-returns-plugin
```

## Usage

Just talk naturally. The skill auto-activates when you mention Amazon returns.

```
"Return my AirPods, drop off at Whole Foods"
"I want to return the keyboard I bought last week, UPS"
"Return my AirPods and the phone case, Kohl's"
```

If you forget to say where to drop off, it'll show you the options:

```
Where do you want to drop it off?
- Whole Foods
- UPS Store
- Kohl's
- Staples
- Amazon Fresh
```

Claude navigates Amazon, finds the order, clicks through the return flow, and stops only at the final submit for your approval.

## How it works

1. You say what to return and where to drop it off
2. Claude navigates to your Amazon orders and finds the item
3. Clicks through the entire return flow automatically
4. Stops at the final confirmation with a one-liner summary
5. You say yes, done — QR code on screen

## Requirements

- Claude Cowork with browser access
- Signed into Amazon in the browser

## Plugin structure

```
.claude-plugin/
  plugin.json          # Plugin manifest
skills/
  amazon-returns/
    SKILL.md           # The skill — all logic in one file
```

## License

MIT
