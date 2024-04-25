1. If we already have it on the `Person` model, return it directly (email/phoneNumber keys)

2. If not, check if we already have searched for it before by looking at the company/person in the `Person` model and checking the date of `searchedContactInfoAt`. If we did search already in the last 30 days, return nothing as it's impossible.

3. If not, apply the required one

**People**: Google Search for `"[full name]" "contact OR email OR phone"` to get a SERP

**Companies**: Google Search for `"[company name]" "contact OR email OR phone"` to get a SERP

4. Analyse the SERP by using a regex for email and one for phone numbers. If nothing is found, use the LLM to find hidden ones (e.g. emails written like contact AT companyname DOT com)

5. If found, store the retreived contact details on the `Person` model on `email` and `phoneNumber` respectively. If not found. Also, set `searchedContactInfoAt` to now.
