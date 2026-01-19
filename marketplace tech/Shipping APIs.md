
I spent some time researching options for shipping APIs, and trying to write integrations for them. It's rare for them to offer first class support for marketplaces.

Shippo seemed the best, and has a special program for marketplaces with 'Platform accounts'
- https://docs.goshippo.com/docs/platformaccounts/platform_accounts/

Recently, I discovered Zonos which is a "Landed cost" shipping API - very relevant today. I think the others can also provide duties, tariffs as part of the cost, this one seems to be for shipping from Canada mostly.

to check also
- Flavorcloud 

## Sendcloud

The best for Europe (i.e. they have th emost options). Their website says they can support marketplaces, detailing a centralized account vs indivudal creator aacount integrations HOWEVER you have to manually onboard each seller's address in your account. opened a ticket with them which confirms this, and said they don't currently have a plan to create a 'create seller address' endpoint.

## Shipstation

https://docs.shipstation.com/getting-started

Not great, currently integrating the API platform under their name which led to confusion folowing docs tutorials, creating accounts. 

## Shippo 

Integration data flow: https://docs.goshippo.com/docs/partner_integration/flow/
Testing strategy: https://docs.goshippo.com/docs/partner_integration/test_plan/

#### Platform Accounts
Marketplaces with merchants should use Platform Accounts
https://docs.goshippo.com/docs/platformaccounts/platform_accounts/

Administering your customers as Managed Shippo Accounts allows you to do the following.
- Customize multiple customers settings behind the scenes that simplifies managing customers at scale . For example, setting up specific carrier accounts to be used for each customer.
- Accurately report on each customer’s activity. For example, obtaining each customer’s associated shipments and other relevant data.

3PLs also called fulfillment centers/warehouses

https://docs.goshippo.com/docs/platformaccounts/platform_upgrade_account/
Have to request upgrade from partnership support team
1. Managed Shippo Accounts do **NOT** automatically inherit access to carriers from your Platform account. To give your Managed Shippo Accounts access to a carrier, you must [add a carrier account to each Managed Account individually](https://docs.goshippo.com/docs/platformaccounts/platform_using_accounts/#how-does-it-work) . You must do this for each carrier you want your Platform account to have access to.

Then you make API calls on behafl of merchants using `SHIPPO-ACCOUNT-ID: <ShippoAccountID>`.

At least you can use the API to create customer accounts, add carriers - no manual step
https://docs.goshippo.com/docs/platformaccounts/platform_using_accounts/#create-a-managed-shippo-account-for-your-customer

