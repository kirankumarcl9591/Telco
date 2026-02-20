### Business Explanation (Telco Subscriber ETL)

In a telecom business, subscriber information comes from multiple operational systems — customer details, address data, city/country mapping, and plan subscriptions.
This data is not always stored in one place and keeps changing as customers update plans, move locations, or new customers join.

The goal of this project is to simulate how a data engineering pipeline supports business reporting and analytics by:

Bringing subscriber-related data from different sources together

Creating a single clean dataset for analysis

Keeping the dataset updated as new changes arrive

 ### Initial Load

At the start, all historical subscriber data is extracted and processed.
This creates a baseline dataset that represents the current state of customers.

### Business value:
Provides a complete view of the customer base for reporting, billing insights, or marketing analysis.

### Incremental Load

After the initial load, only new or changed data is processed.
This reflects updates like:

New subscribers

Plan changes

Address updates

Status changes (active/inactive)

### Business value:
Keeps reporting data fresh without reprocessing everything, saving time and compute cost.

### Merge & Deduplication

Historical and incremental data are combined, and only the latest version of each subscriber record is kept.

### Business value:
Ensures analytics teams always work with accurate and up-to-date customer information.

### Final Outcome

The pipeline produces a curated subscriber dataset that can be used for:

Customer analytics

Revenue/plan analysis

Segmentation

Operational dashboards
