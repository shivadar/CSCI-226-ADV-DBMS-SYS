# C226 / DTD Assignment 2

This repository demonstrates a simple data structure for a Steam user profile, defined with a DTD and validated against sample XML files.


---

### Framework for Data Domain: Steam Gaming Platform

**Decision:**
Which new game should Steam recommend to a user that they are highly likely to purchase and enjoy?

**Signals:**
* **Game Purchase History** (list of owned gameIDs)
* **Recent Playtime** (hours, last 14 days)
* **Wishlisted Games** (current list of gameIDs)
* **User Hardware Specs** (CPU, GPU, RAM; last detected)
* **Friend Activity** (games played by friends; real-time)

**Gaps:**
The primary gap is **external community sentiment**. We don't know which games a user is interested in on platforms like Reddit or Twitch before they wishlist them on Steam. This data would provide an earlier signal of interest.

**Risk:**
The biggest risk is **data staleness**. A recommendation for a graphically intense new game could be made based on hardware specs [Hardware Analytics] that are six months old. If the user has since downgraded their PC, this leads to a poor user experience and a likely refund request.

**Stewardship:**
Access to a user's game library and playtime data must be under explicit user control. The default setting should be "Private," and users must be able to easily change it to "Friends-Only" or "Public." Data should only be retained as long as the user's account is active.

**Data Domain:**
* **Primary:** Gaming Platform (Steam)
* **Adjacent:** E-commerce, Hardware Analytics
