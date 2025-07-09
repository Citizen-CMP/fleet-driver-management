CREATE TABLE vehicles (
    vehicle_id SERIAL PRIMARY KEY,
    license_plate VARCHAR(20) UNIQUE NOT NULL,
    make VARCHAR(50),               -- e.g., Toyota, Ford
    model VARCHAR(50),              -- e.g., Hilux, Ranger
    year INT,                       -- e.g., 2022
    vin VARCHAR(100) UNIQUE,        -- Vehicle Identification Number
    type VARCHAR(50),               -- e.g., Truck, Van, Sedan
    status VARCHAR(20),            -- e.g., Active, In Maintenance, Retired
    mileage INT DEFAULT 0,         -- in kilometers
    fuel_type VARCHAR(20),         -- e.g., Diesel, Gasoline, Electric
    last_service_date DATE,
    next_service_due DATE,
    assigned_driver_id INT,        -- Foreign key to drivers table
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
