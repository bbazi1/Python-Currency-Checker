# Python-Currency-Checker
a simple currency checker with python (USD to every currency)

''import requests as rqs
import string
import time

user_input = ""

response = rqs.get("https://v6.exchangerate-api.com/v6/a2205dfacb804f66b344435e/latest/USD").json()

try_rate = response["conversion_rates"]["TRY"]
eur_rate = response["conversion_rates"]["EUR"]
aed_rate= response["conversion_rates"]["AED"]
  
print(f"USD RATES:\n TRY: {try_rate}\n EUR: {eur_rate}\n AED: {aed_rate}")
print("Use 3-letter ISO currency codes".upper())

while(True): 
    user_input = input("search for any spesific currency or type 'exit' to quit: ")
    if user_input.lower() == "exit":
        break
    else:
        if user_input.upper() in response["conversion_rates"]:
            print(f"{user_input.upper()}: {response["conversion_rates"][user_input.upper()]}")
        else:
            print("unkown currency or wrong input")
            time.sleep(1)''
