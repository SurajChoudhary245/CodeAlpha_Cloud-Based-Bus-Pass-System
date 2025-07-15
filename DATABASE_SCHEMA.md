# 🗃️ Database Schema: `ticket_system`

This database stores all bus pass booking information securely.

## 📌 Table: `bus_passes`

| Column Name     | Data Type     | Description                          |
|-----------------|---------------|--------------------------------------|
| ticket_id       | VARCHAR(20)   | Unique ID generated for each ticket |
| name            | VARCHAR(100)  | Full name of the passenger           |
| email           | VARCHAR(100)  | Email address of the passenger       |
| pass_type       | VARCHAR(50)   | Type of bus pass (e.g., Daily, Monthly) |
| from_location   | VARCHAR(100)  | Starting point of travel             |
| to_location     | VARCHAR(100)  | Destination point                    |
| valid_from      | DATE          | Pass validity start date             |
| valid_till      | DATE          | Pass validity end date               |

---

### ✅ Sample SQL to Create Table

```sql
CREATE TABLE bus_passes (
    ticket_id VARCHAR(20) PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) NOT NULL,
    pass_type VARCHAR(50),
    from_location VARCHAR(100),
    to_location VARCHAR(100),
    valid_from DATE,
    valid_till DATE
);
```