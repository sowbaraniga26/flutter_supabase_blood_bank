```sql
-- 1. request table
CREATE TABLE request (
    id SERIAL PRIMARY KEY,
    recipient_id UUID NOT NULL,
    blood_group VARCHAR(50) NOT NULL,
    quantity_ml INT,
    status VARCHAR(50),
    location VARCHAR(255)
    FOREIGN KEY (recipient_id) REFERENCES users(id) ON DELETE CASCADE,    
);
```