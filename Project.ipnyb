import requests
import json
from requests.exceptions import HTTPError

url = 'https://api.co2signal.com/v1/latest?countryCode=GB'
api_key = '242c3758c804db24'
headers = {'Content-type': 'application/json', 'Accept': 'text/plain', 'auth-token': api_key}

try:
    response = requests.get(url, headers=headers)
        # If the response was successful, no Exception will be raised
    response.raise_for_status()
except HTTPError as http_err:
    print(f'HTTP error occurred: {http_err}')  
except Exception as err:
    print(f'Other error occurred: {err}')
else:
    print('Success!')
data = response.json()
