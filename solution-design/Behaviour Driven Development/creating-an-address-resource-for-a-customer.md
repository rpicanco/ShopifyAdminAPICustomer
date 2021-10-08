<div class="container">
  <h1>Feature: Creating a Customer Resource</h1>
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
  <b>And</b> The system should put the address as default (<code>default = true</code>)<br>
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