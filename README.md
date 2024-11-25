# API Definition
- URL: /api/third_party/user_mapping
- Method: GET
- Authorization HTTP Header: secret-token
- Query Parameters
  +  chain (required): Chain Type, e.g., eth, icp, solana, doge
  +  name (optional): Twitter handle e.g., VlyMoney
  +  scope (required):  e.g., twitter

# Response Data
```json
{
    "code": 200,
    "msg": "success",
    "data": {
        "address": "0x643426BAeCbc7E8fB43d8C590762de632723a04c"
    }
}
```

# Examples（Curl）
```bash
# Get the ICP address of Twitter user VlyMoney
curl --location --request GET 'https://service.vly.money/api/third_party/user_mapping?chain=icp&name=VlyMoney&scope=twitter' --header 'secret-token: YOUR_SECRET_TOKEN'

# Get the Ethereum address of Twitter user VlyMoney
curl --location --request GET 'https://service.vly.money/api/third_party/user_mapping?chain=eth&name=VlyMoney&scope=twitter' --header 'secret-token: YOUR_SECRET_TOKEN'

# Get the Solana address of Twitter user VlyMoney
curl --location --request GET 'https://service.vly.money/api/third_party/user_mapping?chain=solana&name=VlyMoney&scope=twitter' --header 'secret-token: YOUR_SECRET_TOKEN'

# Get the Dogecoin address of Twitter user VlyMoney
curl --location --request GET 'https://service.vly.money/api/third_party/user_mapping?chain=doge&name=VlyMoney&scope=twitter' --header 'secret-token: YOUR_SECRET_TOKEN'
```
