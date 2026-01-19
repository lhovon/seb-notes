# Gotchas

- need to add the admin URL to ADMIN_CORS in the backend `.env`
	- i.e. `http://localhost:9001` or wherever else you run



### Keep in Mind

Internationalization
- french 
- english

User flow of customizing their storefront
User flow of uploading products
Returns and worldwide shipping

guest checkout?


### Things I'll have to build

Not sure I want to use Algolia for search
	- replace with basic postgresql enabled search to start

Chat with TalkJS is super expensive! (300/mo), I'd want to build own solution 
- dont need live chat, just messages


# 2025-12-11 Perusing the code

mercur backend code, while following a medusa integration tutorial gives you ideas of things to search to understand.

Search of `model.define` will reveal all new models 

`extends MedusaService` will show all new services

plugins vs modules - a plugin includes modules, but can also have workflows, admin extensions, providers, etc. 
- though they are under `packages/modules` the mercur extensions are plugins since they have more than just medusa modules.

We have at least 2 onboardings in `b2c-core`: seller onboarding and payout account onboarding
Seller onboaridng has a `stripe_connection` field
