# Naughty-Remote
Adult sexting app (Pro Version)

App created for the non-creative sexter.
Comes with over 50 preset text messages for women and men.
In the app ,, there is an instruction to explain how it works.
This premium version is only $4.99.


<div id="smart-button-container">
      <div style="text-align: center;">
        <div id="paypal-button-container"></div>
      </div>
    </div>
  <script src="https://www.paypal.com/sdk/js?client-id=AU9QweojB6Bo6HQWDQVjN3NxyGPOCfOuAm1lkYQxXyBr7Q1AXdpOqSELkXijXHlmE8ihtW5a7QruhotP&currency=USD" data-sdk-integration-source="button-factory"></script>
  <script>
    function initPayPalButton() {
      paypal.Buttons({
        style: {
          shape: 'pill',
          color: 'gold',
          layout: 'vertical',
          label: 'paypal',
          
        },

        createOrder: function(data, actions) {
          return actions.order.create({
            purchase_units: [{"description":"Naughty Remote APP for android","amount":{"currency_code":"USD","value":4.99}}]
          });
        },

        onApprove: function(data, actions) {
          return actions.order.capture().then(function(details) {
            alert('Transaction completed by ' + details.payer.name.given_name + '!');
          });
        },

        onError: function(err) {
          console.log(err);
        }
      }).render('#paypal-button-container');
    }
    initPayPalButton();
  </script>
  
  
  
  
  
  
  
  
 
