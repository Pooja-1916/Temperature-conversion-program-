# Temperature-conversion-program-
def celsius_to_fahrenheit(celsius):
    return (celsius*9/5)+32
def celsius_to_kelvin(celsius):
    return celsius + 273.15
def fahrenheit_to_celsius(fahrenheit):
    return (fahrenheit-32)*5/9
def fahrenheit_to_kelvin(fahrenheit):
    return (fahrenheit-32)*5/9+273.15
def kelvin_to_celsius(kelvin):
    return kelvin-273.15
def kelvin_to_fahrenheit(kelvin):
    return (kelvin-273.15)*9/5+32
def convert_temperature(value,unit):
    unit=unit.lower()
    if unit=="c":
        fahrenheit=celsius_to_fahrenheit(value)
        kelvin=celsius_to_kelvin(value)
        print(f"\n {value}`C is equal to {fahrenheit:.2f}`F and {kelvin:.2f}K")
    elif unit.lower()=='f':
        celsius=fahrenheit_to_celsius(value)
        kelvin=fahrenheit_to_kelvin(value)
        print(f"\n{value}`F is equal to {celsius:.2f}`C and {kelvin:.2f}K")
    elif unit.lower()=='k':
        celsius=kelvin_to_celsius(value)
        fahrenheit=kelvin_to_fahrenheit(value)
        print(f"\n{value}K is equal to {celsius:.2f}`C and {fahrenheit:.2f}`F")
    else:
        print("\n Invalid unit! Please enter 'C' for Celsius,'F' for Fahrenheit, or 'K' for Kelvin.")
        
temperature=float(input("Enter the temperature value:"))
unit=input("Enter the unit of measurement(C for Celsius, F for Fahrenheit, K for Kelvin):")

convert_temperature(temperature,unit)