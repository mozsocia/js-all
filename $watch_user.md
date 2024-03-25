```js
document.addEventListener('alpine:init', () => {
  Alpine.data('checkoutComponent', () => {
    return {
      main_settings:main_settings[0].fields,
      cartItems: [],
      totalItems: 0,
      totalAmount: 0,
      subTotal: 0,
      delivery_charge: 0,
      selectedDeliveryOption: '',
      discount: 0,
      formData: {
        full_name: '',
        mobile_number: '',
        city: '',
        area: '',
        delivery_address: '',
        delivery_option: 'cash_in_delivery',
        gridCheck1: true ,
      },


      init() {
        this.updateCartFromLocalStorage()
        this.$watch('delivery_charge', (newValue, oldValue) => {
          this.calculateTotals()
          console.log('delivery_charge changed from', oldValue, 'to', newValue)
        })

      },
...
```
