# Mailprotector ROI Calculator

> An unsolicited sales enablement tool built for Mailprotector — a Greenville, SC-based email security company. Helps MSPs quantify the true cost of their current email security stack and model the ROI of switching to Mailprotector.

🌐 **Live:** [View the Calculator](#) *(deploy link goes here)*  
📍 **Built by:** Jennifer Ugarte, Simpsonville, SC  
🏢 **Built for:** [Mailprotector](https://mailprotector.com) — channel-only email security for MSPs

-----

## Why I Built This

Mailprotector is a Greenville-based company I respect — their Partner Centered Thinking philosophy and MSP-exclusive model are rare in the email security space. I built this tool unsolicited because I saw a gap: MSPs switching from Proofpoint, Mimecast, or Barracuda often don’t have a clear, visual way to quantify the full cost of their current stack — licensing, IT time, incident remediation, and ticket overhead combined.

This calculator makes that case instantly, and gives an MSP account rep a shareable, branded leave-behind for every prospect conversation.

It’s also a portfolio piece. I’m a SaaS Implementation Specialist with a background in customer onboarding and technical enablement, and I build tools like this to demonstrate that I think like a product person, not just a project manager.

-----

## What It Does

A fully client-side, zero-backend HTML/JavaScript tool that runs in any browser with no installation required.

### Inputs

|Input                                    |Description                                                                                                     |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------|
|**Number of mailboxes**                  |Total seats to protect                                                                                          |
|**Current vendor**                       |Proofpoint, Mimecast, Barracuda, Microsoft Defender, FortiMail — auto-fills a realistic market price per mailbox|
|**Monthly cost per mailbox**             |Editable — overrides auto-fill if actual pricing is known                                                       |
|**IT hours/month on email security**     |Time spent on management, configuration, troubleshooting                                                        |
|**IT hourly rate**                       |Used to calculate labor cost                                                                                    |
|**Phishing/BEC incidents per year**      |Number of security incidents                                                                                    |
|**Average remediation cost per incident**|IT time + productivity loss + potential breach cost                                                             |
|**Spam/false-positive tickets per month**|Volume of end-user tickets driven by email security issues                                                      |
|**Ticket resolution time (minutes)**     |Used to calculate hidden support overhead                                                                       |
|**Mailprotector plan tier**              |Three plan options with realistic pricing                                                                       |

### Outputs

|Output                       |Description                                                                     |
|-----------------------------|--------------------------------------------------------------------------------|
|**Current annual total cost**|Full TCO: licensing + labor + incidents + ticket overhead                       |
|**Mailprotector annual cost**|Licensing only — Mailprotector’s clean, low-overhead pricing model              |
|**Annual savings**           |Dollar delta                                                                    |
|**ROI %**                    |Return on investment as a percentage                                            |
|**Visual bar chart**         |Side-by-side cost comparison — shareable at a glance                            |
|**Plain-English narrative**  |Auto-generated summary of the findings, ready to paste into an email or proposal|
|**Export to .txt**           |One-click download of the full results summary                                  |

-----

## Design Decisions

### Why client-side only?

No backend, no server, no data storage. The calculator runs entirely in the browser. An MSP rep can open it, fill it in with a prospect on a call, and share the result instantly — with zero setup and zero cost to host.

### Why auto-fill vendor pricing?

MSPs often don’t know their per-mailbox cost off the top of their head — they know the total invoice. Auto-filling a realistic market rate for each vendor gets the conversation started without requiring the prospect to dig up a contract.

### Why include labor and incident costs?

License cost is the visible number. But the total cost of email security includes:

- IT time managing the platform
- Helpdesk tickets from false positives and spam that slips through
- Incident remediation when something actually gets through

Mailprotector’s value proposition isn’t just price — it’s simplicity, lower IT overhead, and fewer incidents. This calculator makes all three visible.

-----

## Tech Stack

|Component|Technology                         |
|---------|-----------------------------------|
|Structure|HTML5                              |
|Logic    |Vanilla JavaScript (no frameworks) |
|Styling  |CSS3 (custom, no library)          |
|Charts   |Chart.js (CDN)                     |
|Export   |Client-side Blob / FileSaver       |
|Hosting  |GitHub Pages or Netlify (free tier)|

Zero dependencies beyond Chart.js. Works offline once loaded.

-----

## File Structure

```
mailprotector-roi-calculator/
├── index.html          # Full application (single file — HTML + CSS + JS)
├── README.md           # This file
└── assets/
    └── mailprotector-logo.png   # Optional: add for branded version
```

-----

## How to Use / Deploy

### Option 1: Run Locally

1. Clone or download this repo
1. Open `index.html` in any browser
1. That’s it — no server needed

### Option 2: Deploy via GitHub Pages (Free)

1. Fork this repo
1. Go to Settings → Pages
1. Set source to `main` branch, root folder
1. Your URL: `yourusername.github.io/mailprotector-roi-calculator`

### Option 3: Deploy via Netlify (Free, Easiest)

1. Go to [netlify.com](https://netlify.com)
1. Drag and drop the `index.html` file
1. Live in under 60 seconds

-----

## Potential Enhancements

- [ ] **PDF export** with Mailprotector branding (printable leave-behind)
- [ ] **MSP multi-tenant view** — model ROI across an entire client book (e.g., 25 clients × 150 seats)
- [ ] **“Share Results” URL** — encode inputs into a URL parameter so a rep can send a pre-filled calculator to a prospect
- [ ] **Email capture** — optional field to send results to the prospect’s inbox
- [ ] **Mailprotector API integration** — pull live pricing directly from the partner portal

-----

## About the Builder

**Jennifer Ugarte**  
SaaS Implementation Specialist | Simpsonville, SC (20 min from Mailprotector HQ)  
Nearly 6 years leading enterprise SaaS implementations at Prism PPM.  
I build tools like this because I think about enablement, onboarding, and adoption — not just execution.

[LinkedIn](https://linkedin.com/in/jenniferugarte1) | [GetSeen.ai](https://getseen.ai)

-----

*This tool was built independently and is not affiliated with or endorsed by Mailprotector. It is offered as an open contribution to their partner and sales community.*
