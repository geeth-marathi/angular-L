# Form Validations

### 

- Input value need to be round to 2 decimals
- Only positive numbers
- Accept Floats

```
        <input
          type="number"
          matInput
          placeholder="Payment Amount"
          formControlName="paymentAmount"
          required
          (change)="updatePaymentButtonTotal()"
          oninput="value == '' ? value = 0 : value < 0 ? value = value * -1 : value = value * 1"
          onchange="value = (value*1).toFixed(2)"
        />
```