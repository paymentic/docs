# Paymentic 

This organization has the main idea to be a fake organization that simulates
a payment gateway product.

The main source of truth for that implementation will be the system design
described at https://newsletter.pragmaticengineer.com/p/designing-a-payment-system

We can change our implementation to met Brazil region characteristics.

## Main components

- **Payment Service:** This is the primary entry point for payment events from users. It conducts an initial risk check to ensure compliance with regulations like AML/CFT and to detect any criminal activities like money laundering. Payments only proceed if they pass this risk assessment.

- **Payment Executor:** Responsible for executing individual payment orders, which can be part of a larger payment event, through a Payment Service Provider (PSP).

- **Payment Service Provider (PSP):** Facilitates the actual movement of money from one account to another, such as from a buyer's credit card account.

- **Card Schemes:** These are the entities like Visa and MasterCard that process credit card operations, operating within a complex ecosystem.

- **Ledger:** Maintains financial records of transactions, crucial for post-payment analysis and financial forecasting.

- **Wallet:** Manages merchant account balances and may track user payment totals.


## Software architecture docs

We are using [c4 model](https://c4model.com/) to describe the software architecture of this project.

The C4 model, as described on c4model.com, is a framework for visualizing software architecture. It provides a systematic approach to create diagrams at four different levels of abstraction:

- **Context Diagrams:** Show the system's context within its environment, including external systems and users.
- **Container Diagrams:** Illustrate the high-level technology choices, software containers, and their interactions.
- **Component Diagrams:** Break down the containers into individual components, detailing their interactions and responsibilities.
- **Code Diagrams:** Provide the most detailed view, focusing on the implementation of specific components.
