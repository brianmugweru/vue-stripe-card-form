vue-stripe-card-form
=============

Form for collecting credit card details and receiving a token from Stripe

## Installation
---------------
##npm
``` sh
npm install --save vue-stripe-card-form
```

Include the stripe script in the head of your index.html file
``` sh
<script type="text/javascript" src="https://js.stripe.com/v2/"></script>
```

Use the component by passing though your stripe publishable key.
The payment tokenReceived event will fire as soon as the form recieves a token from the Stripe API. 
``` sh
<stripe-payment @tokenReceived="gotToken" :stripe-key="[YOU_STRIPE_PUBLISHABLE_KEY_GOES_HERE]">
</stripe-payment>
```

You can get the token in the callback function defined in the tokenReceived event.
``` sh
methods:{
    gotToken(token){
        // Send your token to the server or whatever
    }
}
```
