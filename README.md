# lstore-database-system-overview
L-Store Database System — Architecture Overview
Project Overview
This repository provides an architectural and design overview of a database system inspired by L-Store (Lineage-based Data Store) and modern HTAP (Hybrid Transactional/Analytical Processing) systems.
The original project was developed as part of ECS 165A — Database Systems (UC Davis).
To respect academic integrity policies, the full implementation remains private.
This repository documents the system design, architecture, and technical concepts behind the project.
Motivation
Modern organizations require systems that support both:
OLTP → High-volume transactional workloads
OLAP → Large-scale analytical queries
Traditionally, these workloads required separate systems and data duplication.
HTAP databases solve this by combining both workloads into a single unified architecture.
This project explores how such a system can be designed.
Key Concepts Explored
Hybrid Transactional / Analytical Processing (HTAP)
Unified processing of transactions and analytics
Eliminates ETL pipelines and duplicate storage
Enables real-time analytics on fresh data
L-Store Architecture
Key design ideas:
Column-oriented storage
Tail pages for updates
Lineage tracking
Merge process for performance
Multi-version concurrency control
System Components
Storage Engine
Columnar data layout
Base pages and tail pages
Efficient update handling
Reduced write amplification
Concurrency Control
Multi-version concurrency control (MVCC)
Transaction isolation
Conflict resolution
Indexing
Fast record lookup
Support for analytical scans
Efficient query execution
Query Processing
Supports:
Insert
Update
Delete
Point queries
Range queries
Aggregate queries
Challenges & Lessons Learned
This project provided hands-on experience with:
Designing database storage engines
Tradeoffs between OLTP and OLAP workloads
Concurrency and consistency challenges
Performance vs. complexity decisions
Translating research papers into real systems
Skills Demonstrated
Database architecture
Systems design
Data structures
Performance tradeoff analysis
Technical documentation
Note on Source Code
The full implementation is kept private to comply with course academic integrity policies.
Code can be shared with recruiters upon request.
Author
Nicholas Pinero
Computer Science — UC Davis
