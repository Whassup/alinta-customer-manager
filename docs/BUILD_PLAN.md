# Build Plan

High level features;
1. User can see list of customers.
2. User can search a list of customers by first or last name.
3. User can can add a customer.
4. User can can edit a customer.
5. User can can delete a customer.


## 1. User can see list of customers.

* Create `CustomersView` component to handle the display

enum CustomerManagerDisplay { LIST, SINGLE }

state;
* display: 'LIST' | 'SINGLE'

props;
* customers: CustomerModel;

mapStateToProps;
* customers

* Create `CustomerModel` interface

* Create redux action `Display`

* Create redux action `CreateCustomer`

* Create redux action `UpdateCustomer`

* Create redux action `DeleteCustomer`



* Create redux reducer `customers`

* Create redux reducer `customers`

## 2.User can search a list of customers by first or last name.

* Create redux action `SearchCustomers`

## 3. User can can add a customer.

## 4. User can can edit a customer.

## 5. User can can delete a customer.
