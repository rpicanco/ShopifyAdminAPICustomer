<div>
  <h2>Identify Microservice Boundariess</h2>
  This project have focused on <b>Customer Context</b>, according to <a href="bounded-contexts-context-mapping.md">Bounded Contexts - Context Mapping</a>
  <br><br>
  Each identified domain in Customer Context will be a separated component (microservice). Each microservice in this solution has specific tightly scoped and scalability needs.
  <br><br>
  As an exception, we need to mock the Order microservice just to allow the customer microservice fetch orders. 
</div>

<div>
  <h2>Customer</h2>
  This Microservice is responsible for managing shop's customers information, such as their contact details, whether they've agreed to receive email marketing, status of a customer's account and so on.
</div>

<div>
  <h2>Address</h2>
  This Microservice is responsible for managing customer addresses. We decided to split it out from customer microservice for readability, maintainability and be independently scalable. Moreover, we do not consider it as a Value Object of Customer, because the Address has its own ID been easily independently editable from Customer entity. 
</div>

<div>
  <h2>CustomerSearch</h2>
  This Microservice is responsible for managing saved searches for representing a group of customers defined by the shop owner.
</div>

<div>
  <h2>Order</h2>
  This Microservice is a mock one. It is responsible for giving order information to the customer microservice.
</div>
