# Amazon ATDD Kata
----------------

This is a code kata written for teams that want to practice interacting with Cheezy's pageObject gem. 

Tip: Remember to use test gen to create your initial project structure.

## Feature #1 – Browse Homepage

As a customer, I want to be able to browse Amazon’s homepage so I can see what products are available to sell

<pre>
Scenario: Browse Homepage
  When I browse the homepage
  Then I should see a list of available products
</pre>

Tip: First try doing this with just the simple browser object. Then try this using Cheezy's page object.

## Feature #2 – View A Product

As a customer, I want to be able to view a specific product so I can evaluate if I want to buy it

<pre>
Scenario: Product Details Should Include Key Fields
	When I am on a product detail page
	Then I should see a price, description, and reviews
</pre>

## Feature #3 – Search For Invalid Product

As a customer, I want to get feedback if I search for an invalid product

<pre>
Scenario: Searching For Invalid Products
	Given I am on the Amazon Homepage
	When I search for an invalid product
	Then I should receive a message stating no products were returned
</pre>

## Feature #4 – Search For Valid Product Should Return Results

As a customer, I want to see all products that match the search criteria so that I can then view them

<pre>
Scenario: Searching For Valid Product Should Return Results
	Given I am on the Amazon Homepage
	When I search for a valid product
	Then I should see a list of products
	
Scenario: Search For Valid Product Should Display The Search Term
	Given I am on the Amazon Homepage
	When I search for a valid product
	Then I should see the term searched for
</pre>


