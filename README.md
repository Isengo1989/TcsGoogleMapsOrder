
# TcsGoogleMapsOrder
This plugin will take the billing order zipcode, transfer it to a longitude and latitude and push it with the total amount and icon to your firebase database.

## Used Event
Currently the `CheckoutOrderPlacedEvent` is used to have the best possible reactive solution. This could be inperformant and not 100% accurate since it is triggered before the payment is successful.
You can exchange this event as you like with one that is more suiteable for your usecase e.g. the`CheckoutFinishPageLoadedEvent`

## Passed data

 - shopName (Context Shopname)
 - shopIcon (configurable per saleschannel)
 - locationLat (extracted from the zipcode - no other address data)
 - locationLng (extracted from the zipcode - no other address data)
 -  orderAmount (float, without currency)

:warning: Please check your companies data privacy policy with your data protection officer before you run this in production

## Todos

Add an internal Menu to Marketing to make the map accessible in the admin panel of shopware 6

## Tested Shopware Versions
- 6.4.11.1
- 6.4.12.0
