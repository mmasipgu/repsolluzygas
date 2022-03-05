### This component only works on HA 0.96 and later.

# Custom component for Repsol Luz y Gas
A platform which allows you to get data from Repsol Luz y Gas website.

## Changelog
### Version 1.1 - 05/03/2022:
- Removed 2 sensor: Last Invoice Amount (Numeric) and Last Invoice Status (Boolean).
This fails if you don't have any invoice yet.

### Version 1.1 - 06/12/2021:
- Added 2 new sensors: Last Invoice Amount (Numeric) and Last Invoice Status (Boolean).
Last Invoice Amount (LIA): represents the amount of the last amount.
Last Invoice Status (LIS): it's a boolean that returns if invoice was paid or not.

## Know Limitations
- This component is limited to 1 house - MultiHouses is not working
- Data is updated every 2 hours


## Current Features
- Read data from repsolluzygas.com.
- Multi contracts per house. (only working with 1 house)
- Available sensors: Amount, Consumption, Total Days, Amount Variable, Amount Fixed, Average Daily Cost, Number of contracts


## Installation
Install the component manually by putting the files from `/custom_components/repsolluzygas/` in your folder `<config directory>/custom_components/repsolluzygas/` 

## Screenshot
Repsol Luz y Gas

![Capture](https://user-images.githubusercontent.com/9134036/113559167-33048500-9601-11eb-9bda-8fbb176fa991.PNG)

![Capture1](https://user-images.githubusercontent.com/9134036/113559174-35ff7580-9601-11eb-9756-8e82a9a6ac24.PNG)

![Capture2](https://user-images.githubusercontent.com/9134036/113559177-3861cf80-9601-11eb-8de3-1fc8f7e2cf82.PNG)


## Configuration
**Example configuration.yaml:**

```yaml
sensor:
  - platform: repsolluzygas
    username: <YourEmail>
    password: <Password>
```
