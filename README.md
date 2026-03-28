# L-Store Database System — Architecture Overview
## Project Overview
This repository provides an architectural and design overview of a database system inspired by L-Store (Lineage-based Data Store) and modern HTAP (Hybrid Transactional/Analytical Processing) systems.
The original project was developed as part of ECS 165A: Database Systems at UC Davis.
In order to respect academic integrity policies, the full implementation remains private.
This repository documents the system design, architecture, and technical concepts behind the project.

## Motivation
Modern organizations require systems that support both:
- OLTP → Write-Optimized Systems
- OLAP → Read-Optimized Systems
Traditionally, these workloads required separate systems and data duplication.
HTAP databases solve this by combining both workloads into a single unified database system.
This project explores how such a system can be designed.

# Key Concepts Explored
## Hybrid Transactional / Analytical Processing (HTAP)
- Unified processing of transactions and analytics
- Eliminates ETL pipelines and duplicate storage
- Enables real-time analytics on fresh data
## L-Store Architecture
Key design ideas:
- Column-oriented storage
- Tail pages for updates
- Lineage tracking to see past updates and record versions
- Merge process for performance (combine updated tail pages into new base page)
- Multi-version concurrency control

# System Components
## Storage Engine
- Columnar data layout
- Base pages and tail pages
- Efficient update handling
## Concurrency Control
- Multi-version concurrency control (MVCC)
- Transaction isolation (Strict Two-Phase Locking)
- Conflict resolution
## Indexing
- Fast record lookup
- Efficient query execution
## Query Processing
Supports:
- Insert
- Update
- Delete
- Point queries
- Range queries
- Aggregate queries
## Challenges & Lessons Learned
This project provided hands-on experience with:
- Designing database storage engines
- Tradeoffs between OLTP and OLAP workloads
- Concurrency and consistency challenges
- Performance vs. complexity decisions
- Translating conceptual knowledge of database systems into actual python code
## Skills Demonstrated
- Database architecture
- Systems design
- Data structures
- Technical documentation and Commenting
- Python Coding
## Note on Source Code
The full implementation is kept private to comply with course academic integrity policies.
The full project including all its code can be shared with recruiters upon request.

# Authors
Nicholas Pinero, Sage Dillemuth(sdillemuth@ucdavis.edu), Iris Yuan(iriyuan@ucdavis.edu), Alvin Guo(allguo@ucdavis.edu), Naomi Cohen(nacohen@ucdavis.edu)
Data Science — UC Davis
