# Flow-for-payments
Assuming the role of merchant and using the public API docs, I have tested end-to-end flow for payments.

At first I created an account on razorpay for testing the API and generated the authorization key.
The using that auth key as fields in basic auth in Postman, a POST request is sent to create an order on url https://api.razorpay.com/v1/orders having following structure:
```
{
  "amount": 100,
  "currency": "INR",
  "receipt": "demo order"
}
```
Then took reference from [docs](https://razorpay.com/docs/payments/payment-gateway/web-integration/standard/build-integration/) to do the web integration.
Changed key in options to the key generated on the razorpay website and order_id to the id of the order generated in Postman.
After that I launched the webpage and after clicking the "Pay with Razorpay" button it redirects to the razorpay payment gateway and ask for payment details.
After submitting the details and following necessary steps the payment is marked as captured.
