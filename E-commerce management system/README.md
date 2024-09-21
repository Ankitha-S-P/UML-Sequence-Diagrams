# E-Commerce Management System - Sequence Diagram

## Overview

This repository contains the sequence diagram illustrating the process flow of an **E-Commerce Management System**. It shows the interactions between different components like the **Customer**, **Website**, **Backend**, **Payment Gateway**, and **Delivery System** during a typical online shopping process.

## Sequence Diagram

The sequence diagram outlines the following steps in an e-commerce transaction:

1. **Browse for Products:** The customer browses products on the website. The website fetches product data from the backend and displays it to the customer.
2. **Add to Cart & Checkout:** The customer adds products to their cart and proceeds to checkout by submitting an order.
3. **Payment Information:** The website sends payment details to the payment gateway, and upon successful payment, a confirmation is sent back.
4. **Registration and Delivery:** If the user is registering a new address, the system stores this information and communicates with the delivery system to estimate the delivery date.
5. **Invoice Generation & Confirmation:** Once the transaction is complete, the website generates an invoice and confirms the delivery to the customer.
6. **Error Handling:** If the registration or payment fails, the checkout is marked as failed.

## Components Involved

- **Customer:** Interacts with the website to browse, order, and pay for products.
- **Website:** Fetches and displays products, processes orders, and interacts with the backend, payment gateway, and delivery system.
- **Backend:** Retrieves product details and stores order information.
- **Payment Gateway:** Handles payment processing and confirmation.
- **Delivery System:** Provides an estimated delivery date and manages shipment of orders.

## Notations

- **Actors:** Represent the main components of the system (e.g., Customer, Website, Backend).
- **Messages:** Represent communication between components, such as fetching product details, payment confirmation, and delivery scheduling.
- **Alt Block:** Handles alternate scenarios, like registration success or failure and checkout failure.
- **Loop:** Repetitive processes, such as browsing for products, are captured in loops.

## Usage

This diagram can be used to understand the flow of an e-commerce management system and can serve as a reference for developers working on similar systems. It provides a clear picture of how different components interact and handle core functionalities like browsing, payment processing, and order delivery.
