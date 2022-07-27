Po Models 
POModel - base model containing primary Id
POProductDetail - product details 
PODiscountRule - discount rule, IsEnabled
PODiscountData - Base model representing discount data
POBuy2Get1DiscountData - data model representing data related to buy2get1 rule

Data Access
IUnitOfWork - Representing the database context 
UnitOfWork - Provides data from 

BusinessModels
Template Design pattern - provides basic structure for rule execution
AbstractDiscountRule - Discount rule class containing the structure of rule execution
Buy2Get1DiscountRule - Specific rule provides discount related data and logic specific to this rule
BOCartItem - business model of cart item derived from the input model 

UIModel:
ShoppingCartModel - UI Model getting the input for calculating the price 

Services: 
IDocumentRuleService - Interface exposing methods to retrieve active discount rules 
 DocumentRuleService - class with implementation related to document rules and provides document rule object
IPriceCalculationService - Interface exposing methods to calculate price
 PriceCalculationService - class which calculates the price by applying discount and provides net price

Unit Test: 
Buy2Get1FreeRuleUnitTest - 	Unit tests related to buy 2 get 1 free scenarios

DiscountRuleServiceUnitTest - 	unit test related to retrieving data from DB, 
								provide active discount rule from database

PriceCalculationService - 	Unit Test for Calculating Price 
			 	With no discount
				With Disabled Discount
				With single product with buy2 get1 
				With combination of product with buy2 get 1 
				With combination of product with buy2 get 1 multiple times 
				
