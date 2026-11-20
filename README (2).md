# CLINIQ AI

**A digital learning initiative, part of the AI Literacy Mission.**
Simple, evidence-based AI education for healthcare professionals, in 52 short chapters.
Author: Dr Mamata Panda (MD), Clinical AI Educator

## Files

| File | Purpose |
|---|---|
| `cliniq-ai.html` | The complete website: home page, chapter library and reading pages, with all 52 chapters inside one file. No internet libraries needed. |
| `cliniq-ai-logo.png` | The CLINIQ AI logo, for social sharing and thumbnails. |
| `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `apple-touch-icon.png` | Optional files that let readers add the site to a phone's home screen and read opened chapters offline. Upload them to the same folder as the HTML file. |
| `make_release.py` | Optional script that builds a copy with only Chapters 1 to N, for a strict embargo (see below). |
| `README.md` | This file. |

## What this version is

- The name is now **CLINIQ AI**, described as a digital learning initiative and part of the AI Literacy Mission. The old name and "Issue" wording are gone everywhere.
- The site has a professional website layout: top menu, a home page with a hero banner, latest chapter, "Why CLINIQ AI", how each chapter works, the four-quarter curriculum, an About section with Dr Mamata Panda (MD), Clinical AI Educator, a Responsible use and privacy section, a chapter library with search, and a footer.
- All 52 chapters were reviewed and rewritten one last time in simpler, more general language (see "How the content was reviewed").
- The earlier PDFs for Chapters 1 to 6 are retired because the name and content changed. No PDFs are made.

## Release schedule: every Friday at 9:15 am

- **Chapter 1 opens on Friday 20 November 2026 at 9:15 am India time (IST).**
- **A new chapter opens every Friday after that at 9:15 am IST.** Chapter 52 opens on Friday 12 November 2027.
- Before the opening time the site shows a launch countdown, and every chapter appears as "Opens <date>". Closed chapters cannot be opened. A link to one shows the home page and a note with its opening date.
- Upload the entire `cliniq-ai.html` file once. The schedule is built into the file, so nothing needs to be done each week and nothing needs to be switched on.

**Two assumptions to check.** First, I treated 9:15 am as India time (IST). Second, "every week" means every Friday (7 days apart). For every other Friday, open `cliniq-ai.html`, search for `INTERVAL_DAYS` and change `7` to `14`. For another time or time zone, change `RELEASE_TIME` (see below). All dates update automatically.

### How the schedule works

- On a website, the page reads the web server's date, so a wrong clock on a reader's phone does not matter. If the server cannot be reached, or the file is opened straight from a computer, it uses the device clock.
- The settings are at the start of the script. Search for `RELEASE SCHEDULE`:
  - `START_DATE = '2026-11-20'` is the Friday on which Chapter 1 opens.
  - `INTERVAL_DAYS = 7` is the gap between chapters (7 means every Friday).
  - `RELEASE_TIME = '09:15'` is the time of day, in India time and 24-hour format, when each chapter opens. `'09:15'` means 9:15 am.
  - `MANUAL_RELEASED_UP_TO = null` turns the schedule off if you replace `null` with a number from 0 to 52, for example `26`.

### Important limit

Hiding closed chapters happens in the reader's browser. All 52 chapters are still inside the file, so a technically minded reader could read later ones with "view page source". For a strict embargo, keep the full file private, run `python make_release.py N` (Python 3 needed), for example `python make_release.py 5`, and upload the file it creates (`cliniq-ai-upto-5.html`). In that file the later chapters are removed completely and the schedule is switched off.

### All opening dates

**Quarter 1: Building AI literacy for healthcare**

| Chapter | Title | Opens (Friday, 9:15 am India time) |
|---|---|---|
| 1 | Why Every Doctor Needs AI Literacy | Fri 20 Nov 2026 |
| 2 | Artificial Intelligence Explained for Doctors | Fri 27 Nov 2026 |
| 3 | How Does AI Actually Learn? | Fri 4 Dec 2026 |
| 4 | Generative AI: Beyond ChatGPT | Fri 11 Dec 2026 |
| 5 | Understanding Large Language Models | Fri 18 Dec 2026 |
| 6 | Prompt Engineering for Doctors | Fri 25 Dec 2026 |
| 7 | ChatGPT vs Gemini vs Claude | Fri 1 Jan 2027 |
| 8 | From Search Engines to AI Research Assistants | Fri 8 Jan 2027 |
| 9 | Understanding RAG in Healthcare | Fri 15 Jan 2027 |
| 10 | AI Agents: The Next Evolution | Fri 22 Jan 2027 |
| 11 | Understanding AI Hallucinations | Fri 29 Jan 2027 |
| 12 | Multimodal AI in Healthcare | Fri 5 Feb 2027 |
| 13 | Evaluating AI Tools Before Using Them | Fri 12 Feb 2027 |

**Quarter 2: AI in clinical practice**

| Chapter | Title | Opens (Friday, 9:15 am India time) |
|---|---|---|
| 14 | AI in Clinical Decision Support | Fri 19 Feb 2027 |
| 15 | AI in Pediatric Practice | Fri 26 Feb 2027 |
| 16 | AI in Asthma and Allergy Care | Fri 5 Mar 2027 |
| 17 | AI in Medical Imaging | Fri 12 Mar 2027 |
| 18 | AI in Laboratory Medicine | Fri 19 Mar 2027 |
| 19 | AI-Powered Clinical Documentation | Fri 26 Mar 2027 |
| 20 | Ambient AI and Voice Documentation | Fri 2 Apr 2027 |
| 21 | AI in Preventive Child Healthcare | Fri 9 Apr 2027 |
| 22 | AI in Patient Education | Fri 16 Apr 2027 |
| 23 | AI Chatbots in Healthcare | Fri 23 Apr 2027 |
| 24 | AI in Hospital Management | Fri 30 Apr 2027 |
| 25 | Wearables and Remote Patient Monitoring | Fri 7 May 2027 |
| 26 | Can AI Improve Patient Safety? | Fri 14 May 2027 |

**Quarter 3: AI in medical research and education**

| Chapter | Title | Opens (Friday, 9:15 am India time) |
|---|---|---|
| 27 | AI in Medical Literature Search | Fri 21 May 2027 |
| 28 | AI-Assisted Systematic Reviews | Fri 28 May 2027 |
| 29 | From Clinical Data to Research Paper | Fri 4 Jun 2027 |
| 30 | AI in Biostatistics | Fri 11 Jun 2027 |
| 31 | AI in Scientific Writing | Fri 18 Jun 2027 |
| 32 | AI and Research Integrity | Fri 25 Jun 2027 |
| 33 | AI in Medical Education | Fri 2 Jul 2027 |
| 34 | Building AI-Powered Medical Teaching Materials | Fri 9 Jul 2027 |
| 35 | AI Simulation in Medical Training | Fri 16 Jul 2027 |
| 36 | AI in Pediatric Clinical Research | Fri 23 Jul 2027 |
| 37 | Explainable AI in Clinical Decision-Making | Fri 30 Jul 2027 |
| 38 | Bias in Medical AI | Fri 6 Aug 2027 |
| 39 | Can AI Become a Research Collaborator? | Fri 13 Aug 2027 |

**Quarter 4: Ethics, governance and the future of healthcare**

| Chapter | Title | Opens (Friday, 9:15 am India time) |
|---|---|---|
| 40 | Data Privacy in Healthcare AI | Fri 20 Aug 2027 |
| 41 | India’s DPDP Act and Healthcare AI | Fri 27 Aug 2027 |
| 42 | WHO Principles for Responsible AI in Health | Fri 3 Sep 2027 |
| 43 | AI Governance in Hospitals | Fri 10 Sep 2027 |
| 44 | Cybersecurity for Practicing Physicians | Fri 17 Sep 2027 |
| 45 | Ethical Challenges of AI in Pediatrics | Fri 24 Sep 2027 |
| 46 | Human-in-the-Loop Healthcare | Fri 1 Oct 2027 |
| 47 | Digital Health Transformation in India | Fri 8 Oct 2027 |
| 48 | Why Doctors Must Participate in AI Development | Fri 15 Oct 2027 |
| 49 | Women in Healthcare AI Leadership | Fri 22 Oct 2027 |
| 50 | Building an AI-Ready Hospital | Fri 29 Oct 2027 |
| 51 | The Future of Pediatric Healthcare | Fri 5 Nov 2027 |
| 52 | The AI-Ready Doctor: A Vision for the Future | Fri 12 Nov 2027 |

## How the content was reviewed (final pass)

You asked for one last check of all 52 chapters to remove anything unverified, invented or not evidence-based, in simple language and in a general way. Here is exactly what was done.

1. **Every chapter was rewritten** in a shorter, simpler, more general form. Each keeps the seven-part format, with key terms defined in plain words.
2. **Only facts confirmed earlier against at least two independent sources were kept.** Each chapter was first researched this way. In this pass, anything that came from a single source, an early report that is not peer reviewed, a conference abstract, a company's own claim or a figure I could not confirm twice was removed or turned into a general statement. Examples of what was removed: a tokenizer preprint (Chapter 5), two prompt-sensitivity preprints (Chapter 6), conference-poster details on anaphylaxis (Chapter 16), a small single-study result on autism screening (Chapter 21), a systematic-review preprint on screening accuracy (Chapter 28) and a legal count of US states (Chapter 20).
3. **Numbers were rounded** ("about one in three") and kept to the strongest facts, at most two or three per chapter.
4. **Suggested prompts and "pearl" steps are labelled** as suggested good practice, not research findings. Prompts avoid doses and patient identifiers.
5. **Each chapter lists its sources**, and says where evidence comes from a developer, a funder, an early report or a US-only survey.

**What this review cannot promise.** I cannot guarantee that no error remains. In this final pass I did not re-open every source; I relied on the earlier two-source checks and removed what could not be confirmed that way. Studies and laws change, and some sources are dated 2026. Before you publish, please have a clinician read the chapters that matter most to you, and use the feedback button to correct anything that is wrong. Chapters where a second look is most useful:

- Chapter 41 (India's DPDP Act): general information, not legal advice. Dates and details may be amended.
- Chapter 47 (India's ABDM numbers) and Chapter 52 (AMA survey): official figures that will change.
- Chapter 20 (recording consent) and Chapter 7 (vendor privacy terms): rules and plans change often.
- Chapters 15, 16 and 21 (pediatrics, asthma and allergy): please read with your own expertise.
- A few clearly labelled early or preliminary findings remain where they teach something useful: Chapter 7 (an early report, not peer reviewed, that disagrees with a peer-reviewed study) and Chapter 8 (a 2026 comparison whose authors call it preliminary).
- Chapter 7 compares ChatGPT, Gemini and Claude. It carries a transparency note that Claude, the assistant used for drafting, is one of the tools compared. Delete that line if you prefer.

## Features for readers

- **Mobile app experience:** bottom bar with Previous, Chapters, Share and Next; share sheet (WhatsApp, LinkedIn and so on); text size buttons; dark mode (follows the phone's setting at first); reading progress bar; back-to-top button; header that slides away while reading; "Welcome back" link to the last chapter opened; large tap targets; no sideways scrolling (checked on all 52 chapters in a phone-sized window).
- **Chapter search** in the chapter library.
- **Printing:** only the chapter on screen prints.
- **Add to home screen (optional):** needs https and the extra files in the same folder, with the HTML file still named `cliniq-ai.html`. Android Chrome: menu, then Install app or Add to Home screen. iPhone Safari: Share, then Add to Home Screen. Opened chapters then work offline, and new chapters load when the phone is online.
- **Feedback:** one **Send feedback** button in the footer opens the reader's email app addressed to `allerpe19@gmail.com`, with the chapter number in the subject. The address is visible in the page code, so spam may reach it. If that happens, use a dedicated feedback address.
- **Privacy notice:** the Responsible use and privacy section and the footer say that the site is for education only, no personal identifiers are required, collected or stored, and patient details must never be entered into AI tools. Text size, dark mode and the last chapter opened are saved only on the reader's own device.

## How to publish

1. Upload `cliniq-ai.html` and the logo to your website, for example into `/cliniq-ai/`. For home-screen install and offline reading, also upload `manifest.webmanifest`, `sw.js` and the four icon files into the same folder.
2. Open the page in a browser and check it. WordPress, Wix and Squarespace users can upload the file and embed it with an iframe, or use it as a stand-alone page.

## Standing rules for this series

- Name: **CLINIQ AI**, a digital learning initiative, part of the AI Literacy Mission. Use "Chapter", never "Issue".
- Seven-part format in every chapter; simple language; general, basic education for healthcare professionals.
- Only evidence confirmed against at least two independent sources; no invented, single-source or unverified content; sources listed in each chapter.
- Delivered as the website file and this README only. No PDFs.
- Footer: Dr Mamata Panda (MD), Clinical AI Educator.
