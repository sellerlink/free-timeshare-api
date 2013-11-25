Free & Open API for Timeshare Advertising
=========================================

An innovate way for the many different free classified websites to share certain data and allow the community to communicate and grow together.

Status: Design

Initial design is expected to be live at sellerlink.net sometime in the first quarter of 2014.

Proposals
---------
- Schemas extended from schema.org
- Language agnostic: Widgets in Javascript, PHP, ASP, Python, Node.js, Ruby
- Initially can be driven by scraping and overlaying the API on top of public-facing forms

Architecture:
- Centralized: One trusted host can coordinate the API amongst each website
- Decentralized: The API will coordinate the list of authenticated keys (OAuth) amongst each other
- Must maintain hosts for each site, and versioning or transaction logs for replicating and handling failure gracefully
- Split brain must be handled-each host must only manage its own data..so after being disjoint, it only needs to catch up the peers to its copy

Listing Management:
- REST api for GET/PUT/DELETE
- Should support searching and availability
- Manage distributed listings 
- Can be distinct from website-originated listings

Resort/Hotel Property Management:
- REST api for GET/PUT/DELETE
- Resort, Review, Media (Pictures, Video) distinctions

Messaging:
- REST api for PUT (send offer for listing to website user)
- Obfuscated user ids (sender and receiver) associated with originating website

