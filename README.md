# Contract Data Extension

## Background

This extension adds an object to the contract section that serves us for additional contract information.

## Extension fields

This extension adds a contractDetails property to the contract section of OCDS.
contracts.contractDetails is an object consisting of the following fields:

    • multiyear - Temporality of the commitment (annual or pluriannual). Indicate if the contract covers more than one budget cycle.
    • numberOfMonths - Indicates the number of months and days covered by the contract if it is multi-year.
    • contractType - Name of the type of contract to be concluded.
    • priceScheme - Description of the payment conditions under which contracts may be agreed.

Additional to these fields also has the following four objects with their respective fields:
    
	• minValue - Minimum amount to be paid established in the contract.
		• amount - Numerical number for the minimum amount established in the contract.
		• currency - Acronym of the type of currency in which the minimum value is expressed.

	• maxValue - Maximum amount to be paid established in the contract.
		• amount - Numerical number for the maximum amount established in the contract.
		• currency - Acronym of the type of currency in which the maximum value is expressed.

	• originalCurrencyValue - Total amount of the contract in the type of currency with which you are subscribed.
		• amount - Numerical code for the total amount of the contract in the type of currency with which you are subscribed.
		• currency - Acronym of the type of currency with which the contract is signed.
		• exchangeRate - Exchange rate, if foreign currency, which will be taken for conversion to national currency.

	• fiscalYearValue - When the term of a contract covers more than one cycle, the multi-year amount reflects the amount of money allocated per cycle.
		• amount - Numerical figure for the amount to be disbursed in the fiscal year.
		• currency - Acronym of the type of currency in which the amount to be expended in the fiscal year is expressed.


## Example

```json
"contracts": [{
	"contractDetails": {
		"multiyear": false,
		"numberOfMonths": "0"
		"contractType": "Cerrado",
		"priceScheme": "Variables",
		"minValue": {
			"amount": 0.0,
			"currency": "MXN"
		},
		"maxValue": {
			"amount": 0.0,
			"currency": "MXN"
		},
		"originalCurrencyValue": {
			"amount": 0.0,
			"currency": "MXN",
			"exchangeRate": "1"
		},
		"fiscalYearValue"{
			"amount": 0.0,
			"currency": "MXN"
		}
	}
}]
```
