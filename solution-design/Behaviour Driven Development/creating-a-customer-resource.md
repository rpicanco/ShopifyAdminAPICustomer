<div class="container">
  <h1>Feature: Creating a Customer Resource</h1>
  <div class="panel panel-default">    
    <div class="panel-body"><p style="font-size:100px"><b>In order</b> to manage information about shop's customers<br><b>As</b> a Merchant<br><b>I want</b> to allow my customers ordering products in my shop.</p></div>    
  </div>
</div>

## Scenarios - <img src="success_icon.png" width="100" height="18">

<details>
  <summary>Creating a customer resource with only required fields</summary><br>
  <b>Given</b> There is no customer with email <b><i>robert.smith@example.com</i></b> for the merchant<br>
  <b>And</b> There is no customer with phone <b><i>6135551212</i></b> for the merchant<br>
	<b>And</b> I inform the email <i><b>"robert.smith@example.com"</b></i><br>
	<b>And</b> I inform the first name <b><i>"Robert"</i></b><br>
	<b>And</b> I inform the last name <b><i>"Smith"</i></b><br>
  <b>When</b> I create a customer resource<br>
  <b>Then</b> I should receive a success message confirming customer resource creation<br>
	<b>And</b> The customer doesn't enable its account (<i>state = disabled</i>)<br>
</details>

<details>
  <summary>Creating a customer resource with all default fields</summary><br>
  <b>Given</b> There is no customer with email <b><i>robert.smith@example.com</i></b> for the merchant<br>
  <b>And</b> There is no customer with phone <b><i>6135551212</i></b> for the merchant<br>
	<b>And</b> I inform all fields with default values according to <i><b>OpenAPI Contract</b></i><br>	
  <b>When</b> I create a customer resource<br>
  <b>Then</b> I should receive a success message confirming customer resource creation<br>
	<b>And</b> The customer doesn't enable its account (<i>state = disabled</i>)<br>
</details>

<details>
  <summary>Creating a customer resource with email envite (welcome email) for enabling its account</summary><br>
  <b>Given</b> There is no customer with email <b><i>robert.smith@example.com</i></b> for the merchant<br>
  <b>And</b> There is no customer with phone <b><i>6135551212</i></b> for the merchant<br>
	<b>And</b> I inform all fields with default values according to <i><b>OpenAPI Contract</b></i><br>
  <b>And</b> I inform <code>send_email_invite</code> field with <b><i>"true"</i></b><br>
  <b>When</b> I create a customer resource<br>
  <b>Then</b> I should receive a success message confirming customer resource creation<br>
	<b>And</b> The customer has received an email invite to enable its account (<i>state = invited</i>)<br>
</details>

<details>
  <summary>Creating a customer resource with password and password confirmation and skip sending the welcome email</summary><br>
  <b>Given</b> There is no customer with email <b><i>robert.smith@example.com</i></b> for the merchant<br>
  <b>And</b> There is no customer with phone <b><i>6135551212</i></b> for the merchant<br>
	<b>And</b> I inform all fields with default values according to <i><b>OpenAPI Contract</b></i><br>
  <b>And</b> I inform <code>password</code> field with <b><i>"newpass"</i></b><br>
	<b>And</b> I inform <code>password_confirmation</code> field with <b><i>"newpass"</i></b><br>
  <b>When</b> I create a customer resource<br>
  <b>Then</b> I should receive a success message confirming customer resource creation<br>
	<b>And</b> The customer has enabled its account (<i>state = enabled</i>)<br>
</details>

## Scenarios - <img src="exception_icon.png" width="100" height="18">
