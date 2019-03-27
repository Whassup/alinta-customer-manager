# Build Plan

High level features;
1. User can see list of customers.
2. User can search a list of customers by first or last name.
3. User can can add a customer.
4. User can can edit a customer.
5. User can can delete a customer.


## 1. User can see list of customers.

**1.1** Create `CustomerModel` interface.

**1.2** Create const `customersStub` to be used as customers data.

**1.3** Create redux reducer `customers`.

Data should default to customersStub.

**1.4** Create `CustomersView` component to handle the display of customers list.

Props;
* results: CustomerModel;

Connect redux state and mapStateToProps;
* `state.customers` to `props.results`

Template;
* Add a table to display the customer results

Add component to `App` component

**1.5** Create a styled component for Table 
Apply styled component in `CustomerView` component.

## 2.User can search a list of customers by first or last name.

**2.X** Add search capabilities to `CustomersView`

Update `CustomersView` component;
* add method `search(query: string)`: fires action `SearchCustomers` with query as payload.
* Update `mapStateToProps` to map `state.customerResults` to `props.results`
* Template;
    * add search input as styled component `CustomerSearchBar`. `onKeyPress == Key.Enter` run `CustomersView.search()` 
    * add search button as styled component `CustomerSearchBar`. `onClick` run `CustomersView.search()` 

**2.X** Create redux action `SearchCustomers`

**2.X** Create redux reducer `customerResults`

When is action is of type `SearchCustomers`, 
* If query is defined and not empty return a list of customers with partial matches name matches to the query.
* If query is not defined or empty return all customers. 

**2.X** Update `CustomersView` to the display customer search results




## 3. User can can add a customer.

enum CustomerManagerDisplay { LIST, SINGLE }

state;
* display: 'LIST' | 'SINGLE'

* Create `CustomerDetailsForm` component to inputing properties for a customer

* Create `NewCustomerView` component to for handling adding new customers

* Create redux action `Display`

* Create redux action `CreateCustomer`

## 4. User can can edit a customer.

* Create `EditCustomerView` component to for handling editing new customers

* Create redux action `UpdateCustomer`

## 5. User can can delete a customer.

* Create redux action `DeleteCustomer`
