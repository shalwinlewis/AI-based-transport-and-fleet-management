# Business Requirements Document (BRD)

**Project:** AI-Based Transport & Fleet Management Platform
**Client:** Sumit Road Carriers
**Prepared by:** Shalwin Joel Lewis

---

## 1. Background

Sumit Road Carriers, a transport business with 22 years of operations, managed all fleet, driver, and trip data manually using Excel spreadsheets — tracking only basic information such as driver details, order counts, customer info, and salaries. There was no centralized system for tracking vehicle health, trip status, route efficiency, or profitability, making operations difficult to monitor and scale.

## 2. Stakeholders

- **Primary:** Business owner (sole decision-maker, direct requirements source)
- **Secondary:** Drivers (end users of the driver-facing app)

Requirements were gathered through 4–5 direct conversations with the owner, supplemented by feature requests sent over email.

## 3. Business Objectives

- Centralize fleet, driver, and trip records in one system
- Improve fleet visibility through real-time GPS tracking
- Improve vehicle/driver utilization through smarter assignment
- Reduce fuel and travel costs through route optimization
- Give the owner visibility into revenue, expenses, and trip-level profitability

## 4. Scope

**In scope:**
- Owner and driver logins
- Vehicle, driver, and trip management
- Live GPS tracking
- Route optimization
- Predictive maintenance
- Fuel-efficiency analysis
- AI assistant
- Booking management
- Revenue/profit analytics
- Fleet performance dashboard

**Out of scope:**
- Direct in-platform customer payments — deferred due to the team's lack of payment-integration experience and the risk of transactional errors.

## 5. Functional Requirements

| Role | Key Capabilities |
|---|---|
| Owner | Manage vehicles and drivers, view live tracking, accept/reject bookings, assign vehicle and driver, view maintenance alerts, view revenue/expense/profit analytics |
| Driver | View assigned trip and vehicle, view route, receive route recommendations, report vehicle issues, log fuel data, view trip history |

## 6. Data Requirements

- **Vehicle data:** ID, registration number, age, mileage, load capacity, current status, GPS/device ID
- **Driver data:** ID, name, contact information, license information, assigned vehicle, trip history, performance
- **Trip data:** ID, driver, vehicle, pickup location, destination, distance, load weight, start/end time, route, status
- **GPS data:** speed, direction, timestamp, vehicle status
- **Maintenance data:** vehicle, maintenance type, date, mileage, cost
- **Financial data:** booking amount, fuel cost, maintenance cost, operating expenses, revenue, estimated profit

Data was sourced directly from the owner's real business records (spanning the last 10 years of his 22 years in operation). No customer data, sensitive data, or dummy data was included in the public GitHub repository.

## 7. Assumptions & Constraints

- Fuel/oil price assumed constant year-round (does not yet account for real-world state-by-state and seasonal variation)
- GPS hardware not available on all vehicles at launch
- Minimal budget — free-tier tools and services used wherever possible

## 8. Success Criteria

- Owner gains real-time visibility into vehicle location, delivery status, and driver safety
- Reduction in manual record-keeping effort
- Platform functionally demonstrates the full booking-to-profitability workflow

## 9. Process Flow

1. Customer submits a transport request
2. Owner reviews the booking
3. System checks vehicle and driver availability
4. AI recommends the optimal driver, vehicle, and route (based on distance, traffic, load, fuel requirement, and vehicle condition)
5. Owner assigns the trip
6. Driver is notified and the trip starts
7. GPS streams live vehicle location; AI monitors route deviation, driver behavior, fuel efficiency, ETA, and vehicle health
8. Alerts are generated and sent to owner/driver as needed
9. Trip is completed and stored in trip history
10. Revenue, fuel, and maintenance costs are calculated
11. Profitability analysis is generated, along with AI recommendations

## 10. Outcome

The platform exceeded the client's original expectations — he had initially asked only for a simple system to store records and simplify management. The delivered platform additionally provided predictive maintenance alerts, an AI assistant, and revenue/profit analytics. The client expressed genuine appreciation for the added scope.