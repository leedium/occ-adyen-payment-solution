# Unofficial [Adyen](https://www.adyen.com/ "Adyen ") payment solution for [Oracle Commerce Cloud](https://cloud.oracle.com/en_US/commerce-cloud "Oracle Commerce Cloud")

This is an unoffical work in progress (WIP)  example of an [Adyen](https://www.adyen.com/ "Adyen ") payment solution for
[Oracle Commerce Cloud](https://cloud.oracle.com/en_US/commerce-cloud "Oracle Commerce Cloud") (OCC).  I've taken it upon myself to try and implement the various types of payment methods using features provided by Adyen's [API integration](https://docs.adyen.com/developers/checkout/api-integration "API integration").  This is partly due to the shortcomings of the Out of the box (OOTB) Cybersource soultion packaged with OCC.

*This has only been tested in a test and dev OCC storefront.  
*Please contact me if you would like a demonstration or access to the source. 

### Status
- ~[Visa](https://www.adyen.com/payment-methods/visa), [MasterCard](https://www.adyen.com/payment-methods/mastercard Mastercard), 3D Secure~ WORKING
- ~[Amex](https://www.adyen.com/payment-methods/american-express)~, WORKING
- ~[iDeal(NL)]((https://www.adyen.com/payment-methods "Adyen payment methods") (Netherlands) "iDeal")~ WORKING 
- Interac
- Apple Pay

Current version: 1.00
### Supported Payment Types
- <a href="https://www.adyen.com/payment-methods/visa"><img src="https://www.adyen.com/dam/jcr:0e5869f3-b96e-4843-9efa-1bcd7a101af4/logo-visa.png" alt="visa" height="15px"></a>&nbsp;&nbsp;<a href="https://www.adyen.com/payment-methods/mastercard"><img src="https://www.adyen.com/dam/jcr:c02ee010-d614-400b-88ee-bc1282ac3a3b/master-card.png" alt="mastercard" height="15px"></a>&nbsp;&nbsp;<a href="https://www.adyen.com/payment-methods/american-express"><img src="https://www.adyen.com/dam/jcr:ac9e37d3-543e-4b96-8b68-1aa06d5d2cd4/logo-amex.png" alt="american express" height="15px"></a> Normal and [3DSecure](https://docs.adyen.com/developers/checkout/api-integration/integrate-3d-secure "3D Secure") Credit Card payments
- <a href="https://www.adyen.com/payment-methods/ideal"><img src="https://www.adyen.com/dam/jcr:ab3f0f1d-5fa6-4ab8-87a8-6cba590aa688/logo-ideal.png" height="15px"></a> [local payment](https://www.adyen.com/payment-methods "Adyen payment methods") (Netherlands)
- coming soon Interac (Canada)
- coming soon Apple Pay
- comming recurring payments


#### Includes
- [Server-Side Extension](https://github.com/leedium/occ-adyen/tree/master/sse "Server-side extension")
- [Payment Gateway](https://github.com/leedium/occ-adyen/tree/master/gateway "Payment Gateway")
- [Payment Constants](https://github.com/leedium/occ-adyen/tree/master/widgets/global/constants "Constants")
- [Payment Controller Widget](https://github.com/leedium/occ-adyen/tree/master/widgets/globalController "Global Controller")
- [Payment Authorization Widget](https://github.com/leedium/occ-adyen/tree/master/widgets/authorization "Authorization")
- [Payment Details Widget](https://github.com/leedium/occ-adyen/tree/master/widgets/paymentDetails "Payment Details")

### Technologies
#### UI
- [React](https://reactjs.org/, "react js")
- [knockout.js](https://knockoutjs.com/index.html "knockout.js")
- [javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript, "javascript"),
- [jquery](https://jquery.com/, "jquery")

#### Server
- [Node](https://nodejs.org/ "Node JS")
- [Express](https://expressjs.com/ "Express js").
- [eslint](https://eslint.org/ "Eslint")

#### Testing
- [Mocha](https://mochajs.org/ "Mocha")
- [Expect js](https://github.com/Automattic/expect.js/ "Expect")


### Installation
1. Package and install the [gateway](https://github.com/leedium/occ-adyen/tree/master/gateway "adyen payment gateway for oracle commerce cloud") - /gateway
2. Package and install the [Payment Details](https://github.com/leedium/occ-adyen/tree/master/widgets/paymentDetails "Payment Details")
3. Package and install the [Payment Authorization Widget](https://github.com/leedium/occ-adyen/tree/master/widgets/authorization "Authorization")
** see [occ-react-component](https://github.com/leedium/occ-react-component "occ-react-component") for installation instructions
4. Package and install the [Payment Constants](https://github.com/leedium/occ-adyen/tree/master/widgets/global/constants "Constants") and [Payment Controller Widget](https://github.com/leedium/occ-adyen/tree/master/widgets/globalController "Global Controller") Widgets
** see [occ-react-component](https://github.com/leedium/occ-react-component "occ-react-component") for installation instructions
5. See README.md for installation, test, deploy instructions for the SSE - /sse


1a.  Contact your Adyen Rep and have them enable "raw card data" for PCI compliancy

1b.  Add multiple Origin keys to Adyen
https://docs.adyen.com/developers/checkout/api-integration#multipleoriginkeys

1c. Create a Registered Application Access Token in OCC and add it to the
occAppToken value in the config.  This is used for the test scripts during
deploy
