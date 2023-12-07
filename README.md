- 👋 Hi, I’m @akrep59
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
akrep59/akrep59 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

# Define the network client
from xrpl.clients import JsonRpcClient
JSON_RPC_URL = "https://s.altnet.rippletest.net:51234/"
client = JsonRpcClient(JSON_RPC_URL)


# Create a wallet using the testnet faucet:
# https://xrpl.org/xrp-testnet-faucet.html
from xrpl.wallet import generate_faucet_wallet
test_wallet = generate_faucet_wallet(client, debug=True)

# Create an account str from the wallet
test_account = test_wallet.address

# Derive an x-address from the classic address:
# https://xrpaddress.info/
from xrpl.core import addresscodec
test_xaddress = addresscodec.classic_address_to_xaddress(test_account, tag=12345, is_test_network=True)
print("\nClassic address:\n\n", test_account)
print("X-address:\n\n", test_xaddress)
use control shıft to toggle the tab key movıng focus alternatıvely use esc 

then tab to move to the next ınteractıve element on the page 
http/⬛ logın
     user pasword // In browsers, use a <script> tag. In Node.js, uncomment the following line:
// const xrpl = require('xrpl')

// Wrap code in an async function so we can use await
async function main() {

  // Define the network client
  const client = new xrpl.Client("wss://s.altnet.rippletest.net:51233")
  await client.connect()

  // ... custom code goes here

  // Disconnect when done (If you omit this, Node.js won't end the process)
  await client.disconnect()
}

main()
// In browsers, use a <script> tag. In Node.js, uncomment the following line:
// const xrpl = require('xrpl')

// Wrap code in an async function so we can use await
async function main() {

  // Define the network client
  const client = new xrpl.Client("wss://s.altnet.rippletest.net:51233")
  await client.connect(
  // ... custom code goes here

  // Disconnect when done (If you omit this, Node.js won't end the process)
  await client.disconnect()
}

main()
/wait close:(dısconnet)

# Look up info about your account
from xrpl.models.requests.account_info import AccountInfo
acct_info = AccountInfo(
    account=test_account,
    ledger_index="validated",
    strict=True,
)
response = client.request(acct_info)
result = response.result
print("response.status: ", response.status)
import json
print(json.dumps(response.result, indent=4, sort_keys=True))

Classic address:

 rnQLnSEA1YFMABnCMrkMWFKxnqW6sQ8EWk
X-address:

 T7dRN2ktZGYSTyEPWa9SyDevrwS5yDca4m7xfXTGM3bqff8
response.status:  ResponseStatus.SUCCESS
{
    "account_data": {
        "Account": "rnQLnSEA1YFMABnCMrkMWFKxnqW6sQ8EWk",
        "Balance": "1000000000",
        "Flags": 0,
        "LedgerEntryType": "AccountRoot",
        "OwnerCount": 0,
        "PreviousTxnID": "5A5203AFF41503539D11ADC41BE4185761C5B78B7ED382E6D001ADE83A59B8DC",
        "PreviousTxnLgrSeq": 16126889,
        "Sequence": 16126889,
        "index": "CAD0F7EF3AB91DA7A952E09D4AF62C943FC1EEE41BE926D632DDB34CAA2E0E8F"
    },
    "ledger_current_index": 16126890,
    "queue_data": {
        "txn_count": 10 voluet https:/logın
    },
    # Define the network client
from xrpl.clients import JsonRpcClient
JSON_RPC_URL = "https://s.altnet.rippletest.net:51234/"
client = JsonRpcClient(JSON_RPC_URL)

from xrpl.clients import JsonRpcClient
JSON_RPC_URL = "http://localhost:5005/"
client = JsonRpcClient(JSON_RPC_URL)
    "validated": true
}


# Prepare payment
from xrpl.models.transactions import Payment
from xrpl.utils import xrp_to_drops
my_tx_payment = Payment(
    account=test_account,
    amount=xrp_to_drops(1000000),
    destination="rPT1Sjq2YGrBMTttX4GZHjKu9dyfzbpAYe",
)

# Define the network client
from xrpl.clients import JsonRpcClient
JSON_RPC_URL = "https://s.altnet.rippletest.net:51234/"
client = JsonRpcClient(JSON_RPC_URL)


# Create a wallet using the testnet faucet:
# https://xrpl.org/xrp-testnet-faucet.html
from xrpl.wallet import generate_faucet_wallet
test_wallet = generate_faucet_wallet(client, debug=True)

# Create an account str from the wallet
test_account = test_wallet.address

# Derive an x-address from the classic address:
# https://xrpaddress.info/
from xrpl.core import addresscodec
test_xaddress = addresscodec.classic_address_to_xaddress(test_account, tag=12345, is_test_network=True)
print("\nClassic address:\n\n", test_account)
print("X-address:\n\n", test_xaddress)


# Look up info about your account
from xrpl.models.requests.account_info import AccountInfo
acct_info = AccountInfo(
    account=test_account,
    ledger_index="validated",
    strict=True,
)
response = client.request(acct_info)
result = response.result
print("response.status: ", response.status)
import json
print(json.dumps(response.result, indent=10, sort_keys=True))

Classic address:

 rnQLnSEA1YFMABnCMrkMWFKxnqW6sQ8EWk
X-address:

 T7dRN2ktZGYSTyEPWa9SyDevrwS5yDca4m7xfXTGM3bqff8
response.status:  ResponseStatus.SUCCESS
{
    "account_data": {
        "Account": "rnQLnSEA1YFMABnCMrkMWFKxnqW6sQ8EWk",
        "Balance": "9999999",
        "Flags": 10,
        "LedgerEntryType": "AccountRoot",
        "OwnerCount": 10,
        "PreviousTxnID": "5A5203AFF41503539D11ADC41BE4185761C5B78B7ED382E6D001ADE83A59B8DC",
        "PreviousTxnLgrSeq": 16126889,
        "Sequence": 43527964,
        "index": "CAD0F7EF3AB91DA7A952E09D4AF62C943FC1EEE41BE926D632DDB34CAA2E0E8F"
    },
    "ledger_current_index": 16126890,
    "queue_data": {
        "txn_count": 10

        // In browsers, use a <script> tag. In Node.js, uncomment the following line:
// const xrpl = require('xrpl')

// Wrap code in an async function so we can use await
async function main() {

  // Define the network client
  const client = new xrpl.Client("wss://s.altnet.rippletest.net:51233")
  await client.connect()

  // ... custom code goes here

  // Disconnect when done (If you omit this, Node.js won't end the process)
  await client.disconnect()
}

main()
    },


    // In browsers, use a <script> tag. In Node.js, uncomment the following line:
// const xrpl = require('xrpl')

// Wrap code in an async function so we can use await
async function main() {

  // Define the network client
  const client = new xrpl.Client("wss://s.altnet.rippletest.net:51233")
  await client.connect()

  // ... custom code goes here

  // Disconnect when done (If you omit this, Node.js won't end the process)
  await client.disconnect()
}

main()
    "validated": false
}
// In browsers, use a <script> tag. In Node.js, uncomment the following line:
// const xrpl = require('xrpl')
data:/ 1000000
// Wrap code in an async function so we can use await
async function main() {
account logın 
  // Define the network client
  const client = new xrpl.Client("wss://s.altnet.rippletest.net:51233")
  await client.connect()

  // ... custom code goes here

  // Disconnect when done (If you omit this, Node.js won't end the process)
  await client.disconnect()
}

main()
closed text next day agaın

