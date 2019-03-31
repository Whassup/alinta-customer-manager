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

**2.1** Create redux reducer `customerResults`

Defaults to empty array

**2.2** Create redux action `SearchCustomers`

Update customerResults reducer;

When is action is of type `SearchCustomers`, 
* If query is defined and not empty return a list of customers with partial matches name matches to the query.
* If query is not defined or empty return all customers. 


**2.3** Add search capabilities to `CustomersView`

Update `CustomersView` component;
* add method `search(query: string)`: fires action `SearchCustomers` with query as payload.
* Update `mapStateToProps` to map `state.customerResults` to `props.results`
* on `componentDidMount()` dispatch action `SearchCustomers` to load initial results.
* Template;
    * add search input as styled component `CustomerSearchBar`. `onKeyPress == Key.Enter` run `CustomersView.search()` 
    * add search button as styled component `CustomerSearchBar`. `onClick` run `CustomersView.search()` 

## 3. User can can add a customer.

enum CustomerManagerDisplay { LIST, SINGLE }

state;
* display: 'LIST' | 'SINGLE'

**3.1** Add app routing and assign default root to point to `CustomersView` component.

Also create default root to point to `CustomersView`

**3.2** Add a 'add customer' button to `CustomersView` to that links to route `customer/new`


**3.3** Create redux action `CreateCustomer`

**3.4** Create `NewCustomerView` component to for handling adding new customers

* Add new route to `customers/new` that points to `NewCustomerView`
* Add save and cancel buttons.
* Cancel button should link to root `/`
* Save button should dispatch action `CreateCustomer` and move to route to root.

**3.5** Create `CustomerDetailsForm` component to inputing properties for a customer

state;
* `customer: CustomeModel`

Props;
* `onChange: (customer: CustomerModel)`

Template;
* Create text input fields for first name, last name and DOB and assign their values to `state.customer` onChange and dispatch `props.onChange(customer)`;
* On 

Update `NewCustomerView` to;
* Add `customer` to state. 
* Add `CustomerDetailsForm` into template and bind `onChange` to set new state for customer.
* update `save()` method to include `state.customer` when dispatching action `CreateCustomer`

**3.6** Update reducer `customers` to add customer on action `CreateCustomer`.

**3.7** Validate if customer already exists and provide validation error

Update `NewCustomerView`

mapStateToProps;
* find in  `state.customers` any full name matches in `props.state.customer` and map result to `customerNameInUse`

update `save()` to if `customerNameInUse === true` display error message else dispatch `CreateCustomer`

## 4. User can can edit a customer.

**4.1** Create redux action `UpdateCustomer`

**4.2** Create `EditCustomerView` component to for handling editing new customers

## 5. User can can delete a customer.

* Create redux action `DeleteCustomer`
