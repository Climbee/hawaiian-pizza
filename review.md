- some tests are failing tests
- missing tests, does not test any fail scenarios, no price calculation/discount tests
- using double for price instead of BigDecimal
- no application logging
- mixing responsibilities, e.g. in PurchaseService price calculation and purchase management
- using the same model for ORM and REST API
- passing pizza price via API to add pizza then using the price for purchase calculation
- not fault-tolerant, ongoingPurchases lost after restart, ongoingPurchases is not thread-safe
- no interfaces for services
- a lot of code smells, does not qualify as a clean code


::improvements
- fix add pizza to a purchase, i.e. lookup pizza price instead of passing via API 
- separate pizza price calculation (use discount strategies) since it's likely to change in the future
- add unit tests
