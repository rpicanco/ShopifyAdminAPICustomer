<div class="container">
  <h1>Feature: Creating an address resource for a customer</h1>
  <div class="panel panel-default">    
    <div class="panel-body"><p style="font-size:100px"><b>In order</b> to store address of shop's customers<br><b>As</b> a Merchant<br><b>I want</b> to store address of shop's customers for allowing them to order products in my shop.</p></div>    
  </div>
</div>

<a href="/business-domain-design/functional-requirements.md"><code>FR11</code></a>
<a href="/business-domain-design/functional-requirements.md"><code>FR43</code></a>
<a href="/business-domain-design/functional-requirements.md"><code>FR18</code></a>

## Scenarios - <img src="success_icon.png" width="100" height="18">

<details>
  <summary>Creating the first address resource for a customer with only required fields</summary><br>
  <b>Given</b> The customer is already registered for the merchant<br>
  <b>And</b> there is no address associated with it<br>
  <b>And</b> I inform the <code>customer_id</code><br>
  <b>And</b> I inform the <code>address1</code> <b><i>"1 Rue des Carrieres"</i></b><br>
  <b>And</b> I inform the <code>city</code> <b><i>"Montreal"</i></b><br>
  <b>And</b> I inform the <code>zip</code> <b><i>"G1R 4P5"</i></b><br>
  <b>When</b> I create an address resource for the customer<br>
  <b>Then</b> The system should create the address resource for the customer<br>
  <b>And</b> The system should put the newly address as default (<code>default = true</code>)<br>
  <b>And</b> The system should return a success message confirming address resource creation<br>
</details>

<details>
  <summary>Creating the first address resource for a customer with all fields</summary><br>
  <b>Given</b> The customer is already registered for the merchant<br>
  <b>And</b> there is no address associated with it<br>
  <b>And</b> I inform the <code>customer_id</code><br>
  <b>And</b> I inform the <code>address1</code> <b><i>"1 Rue des Carrieres"</i></b><br>
  <b>And</b> I inform the <code>city</code> <b><i>"Montreal"</i></b><br>
  <b>And</b> I inform the <code>zip</code> <b><i>"G1R 4P5"</i></b><br>
  <b>And</b> I inform all other fields according to <i><b>OpenAPI Contract</b></i><br>
  <b>When</b> I create an address resource for the customer<br>
  <b>Then</b> The system should create the address resource for the customer<br>
  <b>And</b> The system should put the newly address as default (<code>default = true</code>)<br>
  <b>And</b> The system should return a success message confirming address resource creation<br>
</details>

<details>
  <summary>Creating an address resource with only required fields for a customer that already has another address associated with it</summary><br>
  <b>Given</b> The customer is already registered for the merchant
  <b>And</b> there is an address associated with it
  <b>And</b> I inform the <code>customer_id</code><br>
  <b>And</b> I inform the <code>address1</code> <b><i>"1 Rue des Carrieres"</i></b><br>
  <b>And</b> I inform the <code>city</code> <b><i>"Montreal"</i></b><br>
  <b>And</b> I inform the <code>zip</code> <b><i>"G1R 4P5"</i></b><br>
  <b>When</b> I create an address resource for the customer<br>
  <b>Then</b> The system should create the address resource for the customer<br>
  <b>And</b> The system should remove any other addresses as default (<code>default = false</code>)<br>
  <b>And</b> The system should put the newly address as default (<code>default = true</code>)<br>
  <b>And</b> The system should return a success message confirming address resource creation<br>
</details>

<details>
  <summary>Creating an address resource with all fields for a customer that already has another address associated with it</summary><br>
  <b>Given</b> The customer is already registered for the merchant
  <b>And</b> there is an address associated with it
  <b>And</b> I inform the <code>customer_id</code><br>
  <b>And</b> I inform the <code>address1</code> <b><i>"1 Rue des Carrieres"</i></b><br>
  <b>And</b> I inform the <code>city</code> <b><i>"Montreal"</i></b><br>
  <b>And</b> I inform the <code>zip</code> <b><i>"G1R 4P5"</i></b><br>
  <b>And</b> I inform all other fields according to <i><b>OpenAPI Contract</b></i><br>
  <b>When</b> I create an address resource for the customer<br>
  <b>Then</b> The system should create the address resource for the customer<br>
  <b>And</b> The system should remove any other addresses as default (<code>default = false</code>)<br>
  <b>And</b> The system should put the newly address as default (<code>default = true</code>)<br>
  <b>And</b> The system should return a success message confirming address resource creation<br>
</details>

<details>
  <summary>Creating an address resource for a customer that already has four addresses associated with it</summary><br>
  <b>Given</b> The customer is already registered for the merchant<br>
  <b>And</b> there are four addresses associated with it<br>
  <b>And</b> I inform the <code>customer_id</code><br>
  <b>And</b> I inform the <code>address1</code> <b><i>"1 Rue des Carrieres"</i></b><br>
  <b>And</b> I inform the <code>city</code> <b><i>"Montreal"</i></b><br>
  <b>And</b> I inform the <code>zip</code> <b><i>"G1R 4P5"</i></b><br>
  <b>And</b> I inform all other fields according to <i><b>OpenAPI Contract</b></i><br>
  <b>When</b> I create an address resource for the customer<br>
  <b>Then</b> The system should create the address resource for the customer<br>
  <b>And</b> The system should remove any other addresses as default (<code>default = false</code>)<br>
  <b>And</b> The system should put the newly address as default (<code>default = true</code>)<br>
  <b>And</b> The system should return a success message confirming address resource creation<br>
</details>

<details>
  <summary>Creating a second address resource for a customer with all same fields value from the first one</summary><br>
  <b>Given</b> The customer is already registered for the merchant<br>
  <b>And</b> there is an address associated with it<br>
  <b>And</b> I inform the same fields value of address is already associated with it<br>
  <b>When</b> I create an address resource for the customer<br>
  <b>Then</b> The system should create the address resource for the customer<br>
  <b>And</b> The system should remove any other addresses as default (<code>default = false</code>)<br>
  <b>And</b> The system should put the newly address as default (<code>default = true</code>)<br>
  <b>And</b> The system should return a success message confirming address resource creation<br>
</details>


## Scenarios - <img src="exception_icon.png" width="100" height="18">

<details>
  <summary>Creating an address resource for a nonexistent customer</summary><br>
    <b>Given</b> The customer is not registered for the merchant<br>    
    <b>And</b> I inform a random <code>customer_id</code><br>
    <b>And</b> I inform the <code>address1</code> <b><i>"1 Rue des Carrieres"</i></b><br>
    <b>And</b> I inform the <code>city</code> <b><i>"Montreal"</i></b><br>
    <b>And</b> I inform the <code>zip</code> <b><i>"G1R 4P5"</i></b><br>	
    <b>When</b> I create an address resource for the customer<br>
    <b>Then</b> The system should not create the address resource<br>
    <b>And</b> The system should return a message <code>customer not found</code> as error message<br>
</details>

<details>
  <summary>Creating an address resource for a customer from other merchant</summary><br>
    <b>Given</b> The customer is already registered for another merchant<br>    
    <b>And</b> I inform the <code>customer_id</code><br>
    <b>And</b> I inform the <code>address1</code> <b><i>"1 Rue des Carrieres"</i></b><br>
    <b>And</b> I inform the <code>city</code> <b><i>"Montreal"</i></b><br>
    <b>And</b> I inform the <code>zip</code> <b><i>"G1R 4P5"</i></b><br>	
    <b>When</b> I create an address resource for the customer<br>
    <b>Then</b> The system should not create the address resource<br>
    <b>And</b> The system should return a message <code>customer not found</code> as error message<br>
</details>

<details>
  <summary>Creating an address resource without an address1</summary><br>
    <b>Given</b> The customer is already registered for the merchant<br>
    <b>And</b> there is no address associated with it<br>
    <b>And</b> I inform the <code>customer_id</code><br>
    <b>And</b> And I do not inform the <code>address1</code><br>
    <b>And</b> I inform the <code>city</code> <b><i>"Montreal"</i></b><br>
    <b>And</b> I inform the <code>zip</code> <b><i>"G1R 4P5"</i></b><br>	
    <b>When</b> I create an address resource for the customer<br>
    <b>Then</b> The system should not create the address resource<br>
    <b>And</b> The system should return a message <code>address1 is required</code> as error message<br>
</details>

<details>
  <summary>Creating an address resource without a city</summary><br>
    <b>Given</b> The customer is already registered for the merchant<br>
    <b>And</b> there is no address associated with it<br>
    <b>And</b> I inform the <code>customer_id</code><br>
    <b>And</b> I inform the <code>address1</code> <b><i>"1 Rue des Carrieres"</i></b><br>
    <b>And</b> And I do not inform the <code>city</code><br>
    <b>And</b> I inform the <code>zip</code> <b><i>"G1R 4P5"</i></b><br>	
    <b>When</b> I create an address resource for the customer<br>
    <b>Then</b> The system should not create the address resource<br>
    <b>And</b> The system should return a message <code>city is required</code> as error message<br>
</details>

<details>
  <summary>Creating an address resource without a zip</summary><br>
    <b>Given</b> The customer is already registered for the merchant<br>
    <b>And</b> there is no address associated with it<br>
    <b>And</b> I inform the <code>customer_id</code><br>
    <b>And</b> I inform the <code>address1</code> <b><i>"1 Rue des Carrieres"</i></b><br>
    <b>And</b> I inform the <code>city</code> <b><i>"Montreal"</i></b><br>
    <b>And</b> And I do not inform the <code>zip</code><br>	
    <b>When</b> I create an address resource for the customer<br>
    <b>Then</b> The system should not create the address resource<br>
    <b>And</b> The system should return a message <code>city is required</code> as error message<br>
</details>

<details>
  <summary>Creating an address resource without an address1, a city and a zip</summary><br>
    <b>Given</b> The customer is already registered for the merchant<br>
    <b>And</b> there is no address associated with it<br>
    <b>And</b> I inform the <code>customer_id</code><br>
    <b>And</b> And I do not inform the <code>address1</code><br>
    <b>And</b> And I do not inform the <code>city</code><br>
    <b>And</b> And I do not inform the <code>zip</code><br>	
    <b>When</b> I create an address resource for the customer<br>
    <b>Then</b> The system should not create the address resource<br>
    <b>And</b> The system should return messages <code>address1 is required</code>, <code>city is required</code>, <code>zip is required</code> as error message<br>
</details>
