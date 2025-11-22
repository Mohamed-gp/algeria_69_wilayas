# 🇩🇿 Algeria 69 Wilayas Dataset

Complete JSON dataset of all 69 Algerian wilayas (provinces) including the **11 newest wilayas** from November 2025.

## 📄 The Data

**All data is in `main.json`** - Just download and use it!

The file contains:

- ✅ All 69 wilayas (48 original + 10 from 2019 + 11 new from 2025)
- ✅ Coordinates (latitude/longitude) for each wilaya capital
- ✅ Names in English and Arabic
- ✅ Population, area, phone codes, postal codes
- ✅ Regional info and notable features

## 🆕 New 2025 Wilayas

These 11 wilayas were just added in November 2025:

| ID  | English               | Arabic            |
| --- | --------------------- | ----------------- |
| 59  | Aflou                 | أفلو              |
| 60  | Barika                | بريكة             |
| 61  | Ksar Chellala         | قصر الشلالة       |
| 62  | Messaad               | مسعد              |
| 63  | Aïn Oussara           | عين وسارة         |
| 64  | Bou Saâda             | بوسعادة           |
| 65  | El Abiodh Sidi Cheikh | الأبيض سيدي الشيخ |
| 66  | El Kantara            | القنطرة           |
| 67  | Bir El Ater           | بئر العاتر        |
| 68  | Ksar El Boukhari      | قصر البخاري       |
| 69  | El Aricha             | العريشة           |

## 🚀 How to Use

### 1. Download

Just download `main.json` from this repo.

### 2. Use in Your Code

**JavaScript:**

```javascript
const data = require("./main.json");
console.log(data.wilayas); // Array of all 69 wilayas
```

**Python:**

```python
import json
with open('main.json') as f:
    data = json.load(f)
print(data['wilayas'])  # List of all 69 wilayas
```

### 3. Example Data Structure

```json
{
  "id": 16,
  "name": "Algiers",
  "name_ar": "الجزائر",
  "latitude": 36.7538,
  "longitude": 3.0588,
  "elevation": 424,
  "region": "North",
  "population_approx": 3000000
}
```

## � What Each Wilaya Has

- `id` - Wilaya number (1-69)
- `name` - Name in English
- `name_ar` - Name in Arabic
- `latitude` & `longitude` - Coordinates
- `elevation` - Height in meters
- `region` - North, High Plateaus, or Sahara
- `area_km2` - Size
- `population_approx` - Population estimate
- `phone_code` - Area phone code
- `postal_code` - Postal code
- `notable_features` - Tourist sites, landmarks, etc.

## 🎯 Use It For

- Maps and location apps
- Data visualization
- Algerian e-commerce sites
- Educational projects
- Research and statistics

## 📝 License

MIT License - Free to use for anything!

## � Want to Help?

Found an error? Want to add more info? Just open an issue or pull request!

## ⭐ Support

If this helped you, give it a star! ⭐

---

**Made for Algeria** 🇩🇿 | Last updated: November 2025
