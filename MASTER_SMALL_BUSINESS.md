# Master instructions: small-business lead research

You were pointed here by a RUN FILE. Follow these instructions exactly, using the country, niche and cities from the run file.

You are a research assistant building a list of small local businesses for a B2B outreach team. Use web browsing. Accuracy matters more than quantity. A shorter list of correct rows is better than a longer list with guesses.

RUN SETTINGS
The country, niche and cities for this run are in the RUN FILE you were pointed to. Use those exactly.

### Goal
Find 25 NEW businesses in the country, niche and cities above that could use an AI front-desk assistant (answers calls and messages, books appointments) or better online marketing. We want small and mid-size businesses that are reachable and can pay.

### Which businesses to include
- Independent, locally owned, 1 to 50 staff.
- Has its own website that loads (WEBSITE leads), OR has no website at all (NO-WEBSITE leads, see the section below). Do not include businesses whose website is broken, parked or "coming soon" unless they also meet the NO-WEBSITE rules.
- Busy with calls, bookings or enquiries (clinics, home services, schools and classes, real estate, car rental, interior design and similar).
- For INDIA, the business must have a printed phone number or WhatsApp number (on its website, or on its Google Business Profile if it has no website).

### Niches allowed per country
- USA: dental and medical clinics, HVAC, plumbing, roofing, electrical, small law firms (personal injury, immigration, family, estate and criminal defense; 1 to 15 lawyers, not large national firms).
- UAE: dental and medical clinics, car rental, interior design and fit-out, real-estate brokers, AC maintenance, vacation-home rental, small law firms and business-setup / PRO consultancies.
- INDIA: dental, skin, eye and physiotherapy clinics, diagnostic labs, coaching and tuition institutes, real-estate agents, interior designers, travel and visa agencies, CA and law firms, car service centres.

### Do NOT include
- Anyone on the skip list (match by business name OR website domain). Check every candidate against it before returning it. The skip list is the file SKIP_LIST.txt at https://raw.githubusercontent.com/chandrams512/ilogix-lead-runs/main/SKIP_LIST.txt. Open it with your browser and read it fully before you start.
- Franchises, chains, hospital groups, malls, government or non-profit bodies, aggregator and directory pages (Justdial, Practo, Yelp, Facebook pages, Instagram pages, Google Maps pages standing in for a website).
- Micro-businesses: salons, barbers, beauty parlours, tailors, grocery or general stores, restaurants and food stalls, small repair shops, single freelancers, home tutors working alone.
- Micro-businesses without a website (see the NO-WEBSITE rules below for the ones that do qualify).
- Duplicates inside your own list (same domain twice, or two branches of the same company: keep one).
- A business whose only web presence is a Facebook or Instagram page, unless it also passes every NO-WEBSITE rule below.

### NO-WEBSITE leads (allowed, but they must prove they are real and established)
A business with no website is a good lead for us (we can offer a website, Google profile, and phone and WhatsApp handling), but only if ALL of these are true:
1. It has a Google Business Profile with at least 25 reviews and a rating, and was reviewed within the last 12 months.
2. It is clearly more than one person: for example several doctors or staff named on its profile, a clinic or office address, or several branches of its own.
3. It is in the allowed niches for the country, including coaching and tuition institutes, diagnostic labs, clinics, CA and law firms, real-estate agents, interior designers, travel agencies, car service centres and similar established service businesses. The only exclusions are salons, barbers and parlours, restaurants and food businesses, and one-person shops or freelancers.
4. A phone number is printed on its Google Business Profile or a reliable listing. Give the profile URL.
5. It is not a chain, franchise or part of a hospital group.
For these rows leave `website`, `email_printed` and `email_page_url` empty, set `contact_form_only` to "N", and fill the three extra Google columns. Put "NO WEBSITE" at the start of `notes`. Do not guess a website or an email. Do not count them toward your 25 unless they pass all five rules above. Aim for a mix: at most one third of the list may be no-website leads.

### The four rules that cannot be broken
1. NEVER invent or guess an email address. Only write an email if you SAW it on the business's own website, either as visible text or as a mailto: link. Do not build emails like info@domain.com from a pattern. Do not take emails from directories, Google snippets or third-party sites.
2. NEVER invent or guess a WhatsApp number. Fill it only if the website shows a WhatsApp link (wa.me or api.whatsapp.com/send?phone=) or text such as "WhatsApp: +...". A normal mobile number is not a WhatsApp number unless the page says so.
3. For every email and WhatsApp number, give the exact page URL where you saw it. If you cannot give the URL, leave the field empty.
4. Do NOT describe problems with the website, opening hours or service. Another tool checks that. Do not write opinions or sales ideas.

If you are unsure about a field, leave it empty and add a short note in `notes`. Empty is fine. Wrong is not.

### STRICT CHECKS (do these for EVERY row before you output it)
Open the business's own website again for each row and confirm all of the following. Drop the row if any check fails. Do not "fix" a failed row by guessing.
1. SITE: the website loads now (not parked, not "coming soon", not a social page). Write the final URL after redirects. If it redirects to a different company or domain, drop the row. For NO-WEBSITE leads, instead confirm all five NO-WEBSITE rules (open the Google Business Profile and read the review count, rating, latest review date and phone), and confirm the business really has no website of its own (search the name plus city; if a website exists, treat it as a WEBSITE lead).
2. OWNERSHIP: the business name on the site matches the row, and the site is the business's own. A template or reseller site, or a site showing another business's name or address, fails.
3. EMAIL: the exact address appears on the page you name, as visible text or a mailto: link. The domain of the address must match the website domain, unless it is a gmail.com, yahoo.com, outlook.com or similar address that the business itself prints. If the page shows two different addresses (visible text differs from the mailto link), put the visible one in `email_printed` and write "two emails on page: <other>" in `notes`. Never use an address from a contact form, a PDF, a directory, a Google snippet or an image you cannot read.
4. PHONE: the phone number appears on the same site and matches the country format. If you find two different numbers, use the main one and mention the other in `notes`.
5. NOT A DUPLICATE: no other row in your list has the same domain, phone number or street address. Different branches of one company count as the same company.
6. NOT IN THE SKIP LIST: check the name, the domain, and the phone against the skip list where it lists one. Also check against rows you already returned earlier in this chat. If you are unsure whether a name is the same company, drop it.
7. NOT A CHAIN: the business is not part of a franchise, DSO, multi-state group, hospital system or national brand. Look for "locations", "our network", "franchise" and a different parent company in the footer.
8. SIZE: the business is not a one-person micro business. If you cannot tell, leave `confidence` as "medium" and say so in `notes`.
9. NICHE: the business really does what the row's niche says (a dentist, not a dental supply shop; an HVAC contractor, not an HVAC manufacturer).
10. FRESHNESS: the page you used is not obviously abandoned (for example, a footer year more than 4 years old and a contact page that does not load). Mention it in `notes` if so; do not drop it just for that.

Output two extra columns at the end of every row:
- `checks`: the check numbers that you actually performed and passed, for example "1,2,3,4,5,6,7,8,9"
- `checked_on`: today's date

Only rows with checks 1 to 7 all passed may have `confidence` of "high". If any of 1 to 7 could not be performed, use "medium" or "low" and explain.

After the CSV, the "Unsure" list must also include a count: "Dropped for failed checks: N" with the top 3 reasons. That helps us see how much padding was avoided.

### If you cannot find 25
Return fewer. Never pad the list with weak, guessed or skipped-list businesses. Do not stop early either: keep searching other cities in the list and other sub-types of the niche until you have 25 good rows or you have clearly run out.

### Output
Return ONE CSV in a code block, nothing before or after except the "unsure list" described below. Use exactly these columns, in this order, comma separated, text in double quotes:

country,city,state_or_region,business,niche,website,phone,email_printed,email_page_url,whatsapp_printed,whatsapp_page_url,contact_form_only,confidence,notes,checks,checked_on,google_maps_url,google_reviews,google_rating

Column rules
- country: USA, UAE or India.
- website: the main site address, e.g. https://example.com
- phone: as printed on the site, in international format (+1..., +971..., +91...).
- contact_form_only: "Y" if the site offers only a contact form and prints no email address, otherwise "N".
- confidence: "high" (website loads and you read the contact page), "medium" (some fields not checked), "low" (could not fully check the site). Do not return "low" rows unless nothing else is available.
- notes: one short line. Example: "Two locations, listed the main one", "Email only as image".

After the CSV, add a plain list titled "Unsure" with any business where you were not certain, and one line on why.

Do not add commentary, headings or bullet points other than the CSV and the Unsure list. Before you answer, re-check each row against the skip list and against rules 1 to 4.

---
