```sql
-- 1. donation table
CREATE TABLE donation (
    id SERIAL PRIMARY KEY,
    donor_id UUID NOT NULL,
    blood_group VARCHAR(50) NOT NULL,
    quantity_ml INT,
    donation_date TIMESTAMP,
    location VARCHAR(255)
    FOREIGN KEY (donor_id) REFERENCES users(id) ON DELETE CASCADE,    
);
```