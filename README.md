FUTURE_CS_02 — Phishing Email Analysis
Tools Utilized
Google Admin Toolbox – Message Header Analyzer
Used to evaluate SPF, DKIM, and DMARC authentication results, along with email routing paths and delivery timestamps across all 10 samples.
Cisco Talos Intelligence
Leveraged for IP reputation analysis and identification of network ownership for real-world samples (E-01, E-02, E-03).
Gmail “Show Original” Feature
Employed to extract raw email headers from authentic received messages for detailed inspection.
Public GitHub Phishing Datasets
Served as the source for curated phishing samples (E-04 through E-10).
Analysis Methodology

The analysis followed a structured and systematic approach:

Header Analysis
Raw email headers were extracted and analyzed using Google Admin Toolbox to verify SPF, DKIM, and DMARC authentication results.
Sender Domain Verification
The display name of the sender was cross-checked against the actual sending domain (as indicated in angle brackets) to detect spoofing attempts.
Content Examination
Email bodies were reviewed for indicators such as urgency cues, reward-based lures, and the level of personalization in greetings.
Link Inspection
Embedded URLs were examined through raw HTML source analysis without interacting with or activating the links.
IP Reputation Analysis
Sending IP addresses were evaluated using Cisco Talos Intelligence to determine their trustworthiness and historical behavior.
Classification Framework
Each email was assessed using a four-indicator scoring model:
2 or more indicators present → Classified as Phishing
1 indicator present → Classified as Suspicious
0 indicators present → Classified as Safe