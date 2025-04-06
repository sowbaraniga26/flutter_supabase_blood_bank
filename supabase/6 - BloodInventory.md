```
-- 5. blood_inventory table

CREATE TABLE blood_inventory (
    id BIGSERIAL PRIMARY KEY,
    donor_id uuid NOT NULL,
    recipient_id uuid NOT NULL,
    blood_group VARCHAR(100) NOT NULL,
    transaction_date VARCHAR(100) NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (donor_id) REFERENCES users(id) ON DELETE CASCADE,
    FOREIGN KEY (recipient_id) REFERENCES users(id) ON DELETE CASCADE
);
```