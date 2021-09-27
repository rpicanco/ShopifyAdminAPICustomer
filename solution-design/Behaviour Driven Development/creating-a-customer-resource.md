<div class="container">
  <h1>Feature: Creating a Customer Resource</h1>
  <div class="panel panel-default">    
    <div class="panel-body"><p style="font-size:100px"><b>In order</b> to store information about shop's customers<br><b>As</b> a Merchant<br><b>I want</b> to store customer's information for allowing them to order products in my shop.</p></div>    
  </div>
</div>

<a href="/business-domain-design/functional-requirements.md"><code>FR01</code></a>

## Scenarios - <img src="success_icon.png" width="100" height="18">

<details>
  <summary>Creating a customer resource with only required fields</summary><br>
  <b>Given</b> There is no customer with <code>email</code> <b><i>robert.smith@example.com</i></b> for the merchant<br>
  <b>And</b> There is no customer with <code>phone</code> <b><i>6135551212</i></b> for the merchant<br>
  <b>And</b> I inform the <code>email</code> <i><b>"robert.smith@example.com"</b></i><br>
  <b>And</b> I inform the <code>first name</code> <b><i>"Robert"</i></b><br>
  <b>And</b> I inform the <code>last name</code> <b><i>"Smith"</i></b><br>
  <b>When</b> I create a customer resource<br>
  <b>Then</b> The system should create the customer resource<br>
  <b>And</b> The system should put the customer account as disabled (<code>state = disabled</code>)<br>
  <b>And</b> The system should return a success message confirming customer resource creation<br>
</details>

<details>
  <summary>Creating a customer resource with all default fields</summary><br>
  <b>Given</b> There is no customer with <code>email</code> <b><i>robert.smith@example.com</i></b> for the merchant<br>
  <b>And</b> There is no customer with <code>phone</code> <b><i>6135551212</i></b> for the merchant<br>
  <b>And</b> I inform the <code>email</code> <i><b>"robert.smith@example.com"</b></i><br>
  <b>And</b> I inform the <code>first name</code> <b><i>"Robert"</i></b><br>
  <b>And</b> I inform the <code>last name</code> <b><i>"Smith"</i></b><br>
  <b>And</b> I inform all other fields with <code>default values</code> according to <i><b>OpenAPI Contract</b></i><br>	
  <b>When</b> I create a customer resource<br>
  <b>Then</b> The system should create the customer resource<br>
  <b>And</b> The system should put the customer account as disabled (<code>state = disabled</code>)<br>
  <b>And</b> The system should return a success message confirming customer resource creation<br>
</details>

<details>
  <summary>Creating a customer resource with email envite (welcome email) for enabling its account</summary><br>
  <b>Given</b> There is no customer with <code>email</code> <b><i>robert.smith@example.com</i></b> for the merchant<br>
  <b>And</b> There is no customer with <code>phone</code> <b><i>6135551212</i></b> for the merchant<br>
  <b>And</b> I inform the <code>email</code> <i><b>"robert.smith@example.com"</b></i><br>
  <b>And</b> I inform the <code>first name</code> <b><i>"Robert"</i></b><br>
  <b>And</b> I inform the <code>last name</code> <b><i>"Smith"</i></b><br>
  <b>And</b> I inform <code>send_email_invite</code> field with <b><i>"true"</i></b><br>
  <b>And</b> I inform all other fields with <code>default values</code> according to <i><b>OpenAPI Contract</b></i><br>  
  <b>When</b> I create a customer resource<br>
  <b>Then</b> The system should create the customer resource<br>
  <b>And</b> The system should put the customer account as invited (<code>state = invited</code>)<br>
  <b>And</b> The system should return a success message confirming customer resource creation<br>
</details>

<details>
  <summary>Creating a customer resource with password and password confirmation and skip sending the welcome email</summary><br>
  <b>Given</b> There is no customer with <code>email</code> <b><i>robert.smith@example.com</i></b> for the merchant<br>
  <b>And</b> There is no customer with <code>phone</code> <b><i>6135551212</i></b> for the merchant<br>
  <b>And</b> I inform the <code>email</code> <i><b>"robert.smith@example.com"</b></i><br>
  <b>And</b> I inform the <code>first name</code> <b><i>"Robert"</i></b><br>
  <b>And</b> I inform the <code>last name</code> <b><i>"Smith"</i></b><br>	
  <b>And</b> I inform <code>password</code> field with <b><i>"newpass"</i></b><br>
  <b>And</b> I inform <code>password_confirmation</code> field with <b><i>"newpass"</i></b><br>
  <b>And</b> I inform all other fields with <code>default values</code> according to <i><b>OpenAPI Contract</b></i><br>
  <b>When</b> I create a customer resource<br>  
  <b>Then</b> The system should create the customer resource<br>
  <b>And</b> The system should put the customer account as enabled (<code>state = enabled</code>)<br>
  <b>And</b> The system should not store the <code>password</code> in plaintext<br>
  <b>And</b> The system should return a success message confirming customer resource creation<br>
</details>

## Scenarios - <img src="exception_icon.png" width="100" height="18">

<details>
  <summary>Creating a customer resource without an email</summary><br>
    <b>Given</b> There is no customer with <code>email</code> <b><i>robert.smith@example.com</i></b> for the merchant<br>
    <b>And</b> There is no customer with <code>phone</code> <b><i>6135551212</i></b> for the merchant<br>
    <b>And</b> I do not inform an <code>email</code><br>
    <b>And</b> I inform the <code>first name</code> <b><i>"Robert"</i></b><br>
    <b>And</b> I inform the <code>last name</code> <b><i>"Smith"</i></b><br>
    <b>When</b> I create a customer resource<br>
    <b>Then</b> The system should not create the customer resource<br>
    <b>And</b> The system should return a message <code>email is required</code> as error message<br>
</details>

<details>
  <summary>Creating a customer resource without a first name</summary><br>
    <b>Given</b> There is no customer with <code>email</code> <b><i>robert.smith@example.com</i></b> for the merchant<br>
    <b>And</b> There is no customer with <code>phone</code> <b><i>6135551212</i></b> for the merchant<br>
    <b>And</b> I inform the <code>email</code> <b><i>"robert.smith@example.com"</i></b><br>
    <b>And</b> I do not inform a <code>first name</code><br>
    <b>And</b> I inform the <code>last name</code> <b><i>"Smith"</i></b><br>
    <b>When</b> I create a customer resource<br>
    <b>Then</b> The system should not create the customer resource<br>
    <b>And</b> The system should return a message <code>first name is required</code> as error message<br>
</details>

<details>
  <summary>Creating a customer resource without a last name</summary><br>
    <b>Given</b> There is no customer with <code>email</code> <b><i>robert.smith@example.com</i></b> for the merchant<br>
    <b>And</b> There is no customer with <code>phone</code> <b><i>6135551212</i></b> for the merchant<br>
    <b>And</b> I inform the <code>email</code> <b><i>"robert.smith@example.com"</i></b><br>    
    <b>And</b> I inform the <code>first name</code> <b><i>"Robert"</i></b><br>
    <b>And</b> I do not inform a <code>last name</code><br>
    <b>When</b> I create a customer resource<br>
    <b>Then</b> The system should not create the customer resource<br>
    <b>And</b> The system should return a message <code>last name is required</code> as error message<br>
</details>

<details>
  <summary>Creating a customer resource without an email, a first name and a last name</summary><br>
    <b>Given</b> There is no customer with <code>email</code> <b><i>robert.smith@example.com</i></b> for the merchant<br>
    <b>And</b> There is no customer with <code>phone</code> <b><i>6135551212</i></b> for the merchant<br>
    <b>And</b> I do not inform an <code>email</code><br>    
    <b>And</b> I do not inform a <code>first name</code><br>
    <b>And</b> I do not inform a <code>last name</code><br>
    <b>When</b> I create a customer resource<br>
    <b>Then</b> The system should not create the customer resource<br>
    <b>And</b> The system should return messages <code>email is required</code>, <code>first name is required</code>, <code>last name is required</code> as error message<br>
</details>

<details>
  <summary>Creating a customer resource with an email already registered for another customer of the merchant</summary><br>
    <b>Given</b> There is a customer with <code>email</code> <b><i>robert.smith@example.com</i></b> already registered for the merchant<br>
    <b>And</b> There is no customer with <code>phone</code> <b><i>6135551212</i></b> for the merchant<br>
    <b>And</b> I inform the <code>email</code> <b><i>"robert.smith@example.com"</i></b><br>    
    <b>And</b> I inform the <code>first name</code> <b><i>"Robert"</i></b><br>
    <b>And</b> I inform the <code>last name</code> <b><i>"Smith"</i></b><br>
    <b>When</b> I create a customer resource<br>
    <b>Then</b> The system should not create the customer resource<br>
    <b>And</b> The system should return a generic message <code>The customer can't be created</code> as error message<br>
</details>

<details>
  <summary>Creating a customer resource with a phone already registered for another customer of the merchant</summary><br>
    <b>Given</b> There is no customer with <code>email</code> <b><i>robert.smith@example.com</i></b> for the merchant<br>
    <b>And</b> There is a customer with <code>phone</code> <b><i>6135551212</i></b> already registered for the merchant<br>
    <b>And</b> I inform the <code>email</code> <b><i>"robert.smith@example.com"</i></b><br>    
    <b>And</b> I inform the <code>first name</code> <b><i>"Robert"</i></b><br>
    <b>And</b> I inform the <code>last name</code> <b><i>"Smith"</i></b><br>
    <b>And</b> I inform the <code>phone</code> <b><i>"6135551212"</i></b><br>
    <b>When</b> I create a customer resource<br>
    <b>Then</b> The system should not create the customer resource<br>
    <b>And</b> The system should return a generic message <code>The customer can't be created</code> as error message<br>
</details>
