
I surveyed existing tech platforms for marketplaces. Any of the paid ones will cost multiple hundreds per month if you want any kind of customization.

Medusa + MercurJS was the most interesting solution - fully OS, extendable. It's a backend service that handles all core ecommerce operations. It's also a framework to build your own extensions. They did all the hard work of modelling ecommerce. You have the admin API and the Store API. A full environemnt will have the backend api, the admin UI (served from backend) and a storefront integration calling the admin and store APIs.
- https://docs.medusajs.com/api/admin
- https://docs.medusajs.com/api/store 

MercurJS is an extension of Medusa for marketplaces. While it seemed very cool at first, it's not polished, not as well maintained (small team), not well documented, 0 tests! But it's active and could change for the better. The official community is the subgroup 'marketplaces' in the Medusa discord - it is the medusa recommended marketplace extension for medusa.

They add a seller/vendor layer on top of Medusa, and a vendor panel UI.

