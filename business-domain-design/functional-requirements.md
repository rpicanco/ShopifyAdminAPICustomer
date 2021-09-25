<div>
  <h2>Functional Requirements</h2>
	As we know, one of the main benefits of APIs is to hide the backend implementation. Some requirements I was able to identify from Shopify's public API documentation and others requirements I had to assume for our project.<br><br>
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
	<br>
	<li>[<b>FR11</b>] The system must allow Merchants create addresses for their customers. Each customer can have multiple addresses associated with them. If there is no address, the newest one will be the address default.</li>
	<br>
	<li>[<b>FR12</b>] The system must allow Merchants retrieve a customer’s address list.</li>
	<br>
	<li>[<b>FR13</b>] The system must allow Merchants retrieve a single address from a customer.</li>
	<br>
	<li>[<b>FR14</b>] The system must allow Merchants update a single address from a customer.</li>
	<br>
	<li>[<b>FR15</b>] The system must allow Merchants set the default address for a customer.</li>
	<br>
	<li>[<b>FR16</b>] The system must allow Merchants delete a single address from a customer if it is not the default one.</li>
	<br>
	<li>[<b>FR17</b>] The system must allow Merchants delete a customer’s address list except the default one.</li>
	<br>
	<li>[<b>FR18</b>] The system must allow only one address default for a customer.</li>	
	<br>
	<li>[<b>FR19</b>] The system must allow Merchants saved search to represent a "group of customers" defined by the shop owner. In the Shopify admin, the shop owner searches for customers by entering a query and applying one or more filters. When results are returned, the shop owner can save the search and give it a name. After the customer saved search is created, the shop owner can select it at a later date to see a list of customers that match the query.</li>	
	<br>
	<li>[<b>FR20</b>] The system must allow the following customer search advanced queries:</li>
	  <ul>
	    <li>Filter customers by whether they accept email marketing.</li>
	    <li>Retrieve customers from a specified country.</li>
	    <li>Retrieve customers who were created within a set period of time.</li>
	    <li>Retrieve customers who abandoned a cart within a set period of time.</li>
            <li>Retrieve customers who placed an order within a set period of time.</li>
	    <li>Filter customres by the number of orders they've placed with the store.</li>
	    <li>Filter customers by their customer account status.</li>
	    <li>Filter customers by tag. Valid values are any existing customer tag, contained in quotation marks.</li>
	    <li>Filter customers by the total amount that they have spent across all of their orders.</li>
	  </ul>
	<br>
	<li>[<b>FR21</b>] The system must allow Merchants retrieve a list of saved search.</li>	
	<br>
	<li>[<b>FR22</b>] The system must allow Merchants retrieve a single saved search.</li>	
	<br>
	<li>[<b>FR23</b>] The system must allow Merchants retrieve all customers returned by a customer saved search.</li>	
	<br>
	<li>[<b>FR24</b>] The system must allow Merchants retrieve a count of all customer saved searches.</li>	
	<br>
	<li>[<b>FR25</b>] The system must allow Merchants update a customer saved search.</li>	
	<br>
	<li>[<b>FR26</b>] The system must allow Merchants delete a customer saved search.</li>	
	<br>
	<li>[<b>FR27</b>] XXXX.</li>	
	<br>
<ul>
