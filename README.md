# ⚡ Captcha Solver API

> **High-speed, reliable captcha solving API** — Fully automated, no browser required. Pure server-side solving.

---

## 🚀 Features

- ✅ **Blazing Fast** — Average solve time under 2 seconds
- ✅ **Server-Side Only** — No browser, no Selenium, no puppeteer needed
- ✅ **Simple REST API** — One GET request, one token back
- ✅ **API Key System** — Secure per-key balance management
- ✅ **Race Condition Safe** — File locking prevents balance corruption
- ✅ **99.9% Uptime** — Production-grade reliability
- ✅ **Unlimited Concurrency** — Send as many requests as you want

---

## 💰 Pricing

| Plan | Price | Details |
|------|-------|---------|
| **Per Solve** | **$0.10** | Pay only for what you use |
| **Minimum Load** | **$5.00** | 50 solves to get started |

> 🔥 **Volume discounts available** — Contact us for bulk pricing

---

## 📡 API Usage

### Endpoint

```
GET /solver.php?base_url=<BASE_URL>&target_domain=<TARGET_DOMAIN>&api_key=<YOUR_API_KEY>
```

### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `base_url` | string | ✅ | The challenge provider base URL |
| `target_domain` | string | ✅ | The target website domain |
| `api_key` | string | ✅ | Your API key |

### Example Request

```bash
curl "https://api.example.com/solver.php?base_url=https://challenge.example.com&target_domain=example.com&api_key=YOUR_KEY_HERE"
```

### Success Response

```json
{
  "token": "d3021b51-b2c0-4840-319a-f2a02c097f37:EQobebKPw2I2AAAA...",
  "remaining_balance": 49
}
```

### Error Responses

```json
{
  "error": "Invalid API key"
}
```

```json
{
  "error": "Insufficient balance"
}
```

```json
{
  "error": "Missing required parameters: base_url, target_domain, api_key"
}
```

---

## 🔧 Quick Integration Examples

### Python

```python
import requests

response = requests.get("https://api.example.com/solver.php", params={
    "base_url": "https://challenge.example.com",
    "target_domain": "example.com",
    "api_key": "YOUR_API_KEY"
})

data = response.json()
token = data["token"]
print(f"Token: {token}")
print(f"Remaining balance: {data['remaining_balance']}")
```

### Node.js

```javascript
const axios = require('axios');

const { data } = await axios.get('https://api.example.com/solver.php', {
    params: {
        base_url: 'https://challenge.example.com',
        target_domain: 'example.com',
        api_key: 'YOUR_API_KEY'
    }
});

console.log('Token:', data.token);
console.log('Remaining:', data.remaining_balance);
```

### PHP

```php
$response = file_get_contents(
    "https://api.example.com/solver.php?" . http_build_query([
        'base_url' => 'https://challenge.example.com',
        'target_domain' => 'example.com',
        'api_key' => 'YOUR_API_KEY'
    ])
);

$data = json_decode($response, true);
echo "Token: " . $data['token'];
```

### cURL (Bash)

```bash
curl -s "https://api.example.com/solver.php?\
base_url=https://challenge.example.com&\
target_domain=example.com&\
api_key=YOUR_API_KEY" | jq .
```

---

## 📊 Status Codes

| Code | Meaning |
|------|---------|
| `200` | ✅ Success — Token returned |
| `400` | ❌ Missing parameters |
| `403` | 🔒 Invalid API key or no balance |
| `500` | ⚠️ Server error |

---

## 🛡️ Security

- 🔐 AES-256-GCM encrypted signal payloads
- 🔑 Unique API keys with individual balance tracking
- 🔒 File-locking to prevent race conditions and double-spending
- 📝 Full request logging per key

---

## 📈 Why Choose Us?

| Feature | Us | Competitors |
|---------|----|-------------|
| Price per solve | **$0.10** | $0.50 - $2.00 |
| Solve speed | **< 2s** | 5 - 30s |
| Browser required | **No** | Usually yes |
| Setup time | **5 minutes** | Hours |
| Concurrency | **Unlimited** | Rate limited |

---

## 📞 Contact & Purchase

| | |
|---|---|
| 💬 **Telegram** | [@void_ether](https://t.me/void_ether) |
| 💰 **Payment** | Crypto (USDT, BTC, ETH, LTC) |
| ⚡ **Delivery** | API key delivered instantly after payment |

---

## 🛒 How to Get Started

1. 💬 **Message us** on Telegram [@void_ether](https://t.me/void_ether)
2. 💳 **Send payment** (minimum $5.00 for 50 solves)
3. 🔑 **Receive your API key** instantly
4. 🚀 **Start solving** — integrate with one line of code

---

## ❓ FAQ

**Q: How fast is the solving?**
> Average under 2 seconds per solve.

**Q: Do I need a browser or headless Chrome?**
> No. It's a pure server-side API. One HTTP request is all you need.

**Q: Can I use this concurrently?**
> Yes. No rate limits. Send as many parallel requests as you need.

**Q: What happens when my balance runs out?**
> You'll get an `Insufficient balance` error. Top up via Telegram to continue.

**Q: Is there a trial?**
> Contact us on Telegram to discuss trial options.

**Q: What payment methods do you accept?**
> USDT (TRC20/ERC20), BTC, ETH, LTC. Other methods available on request.

---

<div align="center">

### ⚡ Stop wasting time on captchas. Start solving now.

**💬 [@void_ether](https://t.me/void_ether) on Telegram**

---

*© 2026 Captcha Solver API. All rights reserved.*

</div>
