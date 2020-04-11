<div id="paypal-button-container"></div>
<script src="https://www.paypal.com/sdk/js?client-id=AelWsmg_xNwoOkZbEWVX2mobTg8MYKilIwlPMusJMIiV-BHw_bSqkm95B30bEZD3vfiBU4y8zTGm3k5w&vault=true" data-sdk-integration-source="button-factory"></script>
<script>
  paypal.Buttons({
      style: {
          shape: 'rect',
          color: 'gold',
          layout: 'vertical',
          label: 'subscribe',
          
      },
      createSubscription: function(data, actions) {
        return actions.subscription.create({
          'plan_id': 'P-45016762VR3649323L2JA5OQ'
        });
      },
      onApprove: function(data, actions) {
        alert(data.subscriptionID);
      }
  }).render('#paypal-button-container');
</script>
