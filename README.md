# 🌊 Vibe Affirmations API

![RapidAPI Status](https://img.shields.io/badge/Hosted_on-RapidAPI-blue?style=for-the-badge)
![Uptime](https://img.shields.io/badge/Uptime-99.9%25-green?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

**Add context-aware affirmations to your apps, bots, and dashboards.**

Most quote APIs are generic. **Vibe Affirmations** serves content based on the *mood* or *context* of your user. whether they need to focus, chill out, or get hyped up.

### 🚀 [**Get Your Free API Key Here**](https://rapidapi.com/user/apiarylabs)

---

## ✨ Features

* **Context Aware:** Filter affirmations by vibe (e.g., `focus`, `chill`, `confidence`).
* **Lightweight:** JSON responses < 1kb.
* **Fast:** Serverless architecture hosted on AWS Lambda via RapidAPI.
* **Free Tier:** Generous free monthly quota for developers and hobbyists.

---

## 🔌 Endpoints

### 1. Get a Random Affirmation
Returns a single random affirmation from any category.
`GET /random`

### 2. Get by Vibe
Returns an affirmation specific to a mood.
`GET /vibe/{category}`

**Available Categories:**
* `confidence`
* `chill`
* `focus`
* `hype`
* *(More coming soon)*

---

## 💻 Usage Examples

### JavaScript (Fetch)
```javascript
const getVibe = async () => {
  const url = '[https://vibe-affirmations.p.rapidapi.com/vibe/confidence](https://vibe-affirmations.p.rapidapi.com/vibe/confidence)';
  const options = {
    method: 'GET',
    headers: {
      'x-rapidapi-key': 'YOUR_API_KEY_HERE',
      'x-rapidapi-host': 'vibe-affirmations.p.rapidapi.com'
    }
  };

  try {
    const response = await fetch(url, options);
    const result = await response.json();
    console.log(result);
  } catch (error) {
    console.error(error);
  }
};

getVibe();
