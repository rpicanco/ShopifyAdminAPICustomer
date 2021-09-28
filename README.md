# ShopifyAdminAPICustomer
This project aims to propose a software development process framework giving insights in how we can split it out in steps using an agile software development methodology. It starts from understanding the business domain using domain-driven design practices to deploy the solution in a production-ready environment. We will design and develop a solution of a public API from shopify for demonstrating the framework proposal as well as some patterns in action, such as Domain-Driven Design, API Gateway, RESTful API Design, Async API, Microservice Architecture, Sync and Async communication, Event-Driven, pub/sub and request-reply messaging pattern, Hexagonal architecture, and much more.<br>

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
       <a>Development Process</a>
    </li>
    <ul>
      <li>
        <a href="#business-domain-design">Business Domain Design</a>
      </li>
      <li>
        <a href="#solution-design">Solution Design</a>
      </li>
      <li>
        <a href="#architecture">Architecture</a>
      </li>
	  <li>
        <a href="#development">Development</a>
      </li>
    </ul>
  </ol>
</details>

## About the Project

This project was based on <a href="https://shopify.dev/api/admin-rest/2021-07/resources/customer">Customer API</a> from <a href="https://shopify.dev/api/admin">Shopify Admin API</a>.

## Business Domain Design

This section aims to understand the business domain, identifying the subdomains and defining the bounded context mapping using Domain-Driven Design practices. In addition, this section is where we register the functional requirements and identify microservice boundaries that will be part of the solution.
<br><br>[Business Domain Design](business-domain-design/business-domain-design.md)

## Solution Design

This section aims to define a solution based on the business domain design section, creating deliverables that will give support for the solution architecture and development itself.
<br><br>[Solution Design](solution-design/solution-design.md)

## Architecture

This section aims to define the solution architecture as well as register all architectural decisions, giving support to the solution development.
<br><br>[Architecture](architecture/architecture.md)

## Development

This section aims to create all deliverables needed to develop the solution, such as detailed flow specifications for each component from the solution, infrastructure as code (IaC) artifacts and the source code itself.
<br><br>[Development](development/development.md)


