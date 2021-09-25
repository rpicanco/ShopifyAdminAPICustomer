<div>
  <h2>Functional Requirements</h2>
	As we know, one of the main benefits of APIs is hide of backend implementation. Some requirements I was able to highlight from Shopify's public API documentation and others requirements I had to assume for our project.<br><br>
</div>

<ul>
	<li>[<b>FR01</b>] The system must allow Merchants create customer resource for storing information about a shop's customers, such as their contact details, their order history, and whether they've agreed to receive email marketing. The Customer resource also holds information on the status of a customer's account. Customers with accounts save time at checkout when they're logged in because they don't need to enter their contact information.</li>
	<br>
	<li>[<b>FR02</b>] The system must allow Merchants generate an account activation URL for a customer whose account is not yet enabled. The account activation URL generated is for one-time use and will expire after 30 days. If the Merchant generate a new account activation URL, then the new URL will be again valid for 30 days, but the previous URL will no longer be valid.</li>
	<br>
	<li>[<b>FR03</b>] The system must allow Merchants send an account invite to their customers.</li>
	<br>
	<li>[<b>FR04</b>] The system must allow Merchants retrieve a list of customers from its portfolio.</li>
	<br>
	<li>[<b>FR05</b>] The system must allow Merchants retrieve a single customer from its portfolio.</li>
	<br>
	<li>[<b>FR06</b>] The system must allow Merchants retrieve all orders belonging to a customer.</li>
	<br>
	<li>[<b>FR07</b>] The system must allow Merchants know how many customers are in its portfolio.</li>
	<br>
	<li>[<b>FR08</b>] The system must allow special Merchants to search for their customer by entering an advanced query.</li>
	<br>
	<li>[<b>FR09</b>] The system must allow Merchants update their customers from its portfolio.</li>
	<br>
	<li>[<b>FR10</b>] The system must allow Merchants delete their customers from its portfolio if they have no existing orders.</li>
<ul>
