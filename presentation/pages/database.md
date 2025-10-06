# What database?
- Time Series
- Cloud-Native IoT Data Platform
- Relational
- NoSQL

---

# Relational Database
- ACID compliance
- Easy to model relationships
- Works well for structured, predictable data
- Not ideal for high-frequency time-series data (may require complex partitioning or table design).
- Can become slow or expensive to scale horizontally

---

# Time-Series Databases
- Optimized for handling large volumes of timestamped data (like telemetry).
- Efficient storage and compression for continuous data streams.
- Less suited for complex relational queries
- Smaller ecosystem and fewer general-purpose tools compared to SQL databases.

---

# NoSQL Databases
- Flexible schema for evolving telemetry data formats
- Good for storing semi-structured or nested data
- Weaker consistency (depending on configuration)
- Querying and analytics can be more limited or less efficient than SQL/time-series solutions.

---

# Cloud-Native IoT Data Platforms 
- e.g. AWS IoT Core + Timestream, Azure IoT Hub + Data Explorer
- Managed ingestion pipelines, device management, and built-in time-series storage
- Scales automatically with little operational effort
- Expensive 
- Less control over storage architecture.
- May require cloud connectivity

---

# Most Suitable
- Time-Series Database (e.g., TimescaleDB or InfluxDB)
- Efficient ingestion and querying of continuous telemetry data
- Retention management for old data
- Easy integration with visualization and alerting tools (like Grafana)
