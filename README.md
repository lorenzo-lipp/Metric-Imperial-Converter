# Metric-Imperial Converter

- This API converts from the metric system to the imperial system and vice versa.

- Since this is a backend pactice, the interface is just for testing and provided by FreeCodeCamp.

Technologies used: Javascript, NodeJS, ChaiJS

# Live Version

![image](./images/preview.png)

# Running Locally

To run this locally, run the following commands in a terminal:

```
npm install
npm start
```

# Requirements

Write the following tests in tests/1_unit-tests.js:

- convertHandler should correctly read a whole number input.
- convertHandler should correctly read a decimal number input.
- convertHandler should correctly read a fractional input.
- convertHandler should correctly read a fractional input with a decimal.
- convertHandler should correctly return an error on a double-fraction (i.e. 3/2/3).
- convertHandler should correctly default to a numerical input of 1 when no numerical input is provided.
- convertHandler should correctly read each valid input unit.
- convertHandler should correctly return an error for an invalid input unit.
- convertHandler should return the correct return unit for each valid input unit.
- convertHandler should correctly return the spelled-out string unit for each valid input unit.
- convertHandler should correctly convert gal to L.
- convertHandler should correctly convert L to gal.
- convertHandler should correctly convert mi to km.
- convertHandler should correctly convert km to mi.
- convertHandler should correctly convert lbs to kg.
- convertHandler should correctly convert kg to lbs.

Write the following tests in tests/2_functional-tests.js:

- Convert a valid input such as 10L: GET request to /api/convert.
- Convert an invalid input such as 32g: GET request to /api/convert.
- Convert an invalid number such as 3/7.2/4kg: GET request to /api/convert.
- Convert an invalid number AND unit such as 3/7.2/4kilomegagram: GET request to /api/convert.
- Convert with no number such as kg: GET request to /api/convert.

Other requirements:

- You can GET /api/convert with a single parameter containing an accepted number and unit and have it converted. (Hint: Split the input by looking for the index of the first character which will mark the start of the unit)
- You can convert 'gal' to 'L' and vice versa. (1 gal to 3.78541 L)
- You can convert 'lbs' to 'kg' and vice versa. (1 lbs to 0.453592 kg)
- You can convert 'mi' to 'km' and vice versa. (1 mi to 1.60934 km)
- All incoming units should be accepted in both upper and lower case, but should be returned in both the initUnit and returnUnit in lower case, except for liter, which should be represented as an uppercase 'L'.
- If the unit of measurement is invalid, returned will be 'invalid unit'.
- If the number is invalid, returned will be 'invalid number'.
- If both the unit and number are invalid, returned will be 'invalid number and unit'.
- You can use fractions, decimals or both in the parameter (ie. 5, 1/2, 2.5/6), but if nothing is provided it will default to 1.
- Your return will consist of the initNum, initUnit, returnNum, returnUnit, and string spelling out units in the format '{initNum} {initUnitString} converts to {returnNum} {returnUnitString}' with the result rounded to 5 decimals.
- All 16 unit tests are complete and passing.
- All 5 functional tests are complete and passing.