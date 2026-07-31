# 🇩🇿 Algeria 69 Wilayas & 1,541 Communes Dataset

Complete JSON dataset of all **69 Algerian wilayas** (provinces) and all **1,541 communes** (municipalities), using the **official government numbering** — including the 11 newest wilayas from November 2025.

## 📄 The Data

| File            | Contents                                                        |
| --------------- | --------------------------------------------------------------- |
| `main.json`     | All 69 wilayas with coordinates, regions, and details           |
| `communes.json` | All 1,541 communes with Arabic names, dairas, and wilaya links  |

- ✅ All 69 wilayas (48 original + 10 from 2019 + 11 new from 2025)
- ✅ All 1,541 communes with their daira (district)
- ✅ **Official numbering** (Loi 19-12 for wilayas 49–58, Loi 26-06 for 59–69)
- ✅ Names in English/French and Arabic
- ✅ Coordinates (latitude/longitude) for each wilaya capital
- ✅ Region classification (North, High Plateaus, Sahara) for every wilaya
- ✅ Commune count per wilaya

## 🆕 New 2025 Wilayas (Official Numbering)

These 11 wilayas were added in November 2025. Numbering follows the official law (Loi 26-06):

| ID  | English               | Arabic            | Split from |
| --- | --------------------- | ----------------- | ---------- |
| 59  | Aflou                 | أفلو              | Laghouat   |
| 60  | El Abiodh Sidi Cheikh | الأبيض سيدي الشيخ | El Bayadh  |
| 61  | El Aricha             | العريشة           | Tlemcen    |
| 62  | El Kantara            | القنطرة           | Biskra     |
| 63  | Barika                | بريكة             | Batna      |
| 64  | Bou Saâda             | بوسعادة           | M'Sila     |
| 65  | Bir El Ater           | بئر العاتر        | Tébessa    |
| 66  | Ksar El Boukhari      | قصر البخاري       | Médéa      |
| 67  | Ksar Chellala         | قصر الشلالة       | Tiaret     |
| 68  | Aïn Oussera           | عين وسارة         | Djelfa     |
| 69  | Messaad               | مسعد              | Djelfa     |

## 🚀 How to Use

### JavaScript

```javascript
const { wilayas } = require("./main.json");
const { communes } = require("./communes.json");

// All 69 wilayas
console.log(wilayas.length); // 69

// All communes of Algiers (wilaya 16)
const algiersCommunes = communes.filter((c) => c.wilaya_id === 16);

// Build a wilaya -> communes dropdown (common e-commerce use case)
const byWilaya = Object.groupBy(communes, (c) => c.wilaya_id);
```

### Python

```python
import json

with open('main.json') as f:
    wilayas = json.load(f)['wilayas']
with open('communes.json') as f:
    communes = json.load(f)['communes']

# All communes of Oran (wilaya 31)
oran = [c for c in communes if c['wilaya_id'] == 31]
```

### Data Structures

**Wilaya** (`main.json`):

```json
{
  "id": 16,
  "name": "Algiers",
  "name_ar": "الجزائر",
  "latitude": 36.7538,
  "longitude": 3.0588,
  "elevation": 424,
  "region": "North",
  "population_approx": 3000000,
  "commune_count": 57
}
```

**Commune** (`communes.json`):

```json
{
  "id": 486,
  "wilaya_id": 16,
  "name": "Bab El Oued",
  "name_ar": "باب الوادي",
  "daira": "Bab El Oued",
  "daira_ar": "باب الوادي"
}
```

## 📋 Field Reference

**Every wilaya has:** `id` (official number 1–69), `name`, `name_ar`, `established`, `latitude`, `longitude`, `elevation`, `region`, `commune_count`.

**Some wilayas also have:** `area_km2`, `population_approx`, `phone_code`, `postal_code`, `notable_features`, `parent_wilaya` + `new_2025` (for the 2025 wilayas), `coastal`, `capital`.

**Every commune has:** `id`, `wilaya_id` (matches `main.json` ids), `name`, `name_ar`, `daira`, `daira_ar`.

## 🖥️ Live Demo

**[mohamed-gp.github.io/algeria_69_wilayas](https://mohamed-gp.github.io/algeria_69_wilayas/)** — browse and search all wilayas and communes interactively (search works on commune names too). The JSON files are also served there directly:

- `https://mohamed-gp.github.io/algeria_69_wilayas/main.json`
- `https://mohamed-gp.github.io/algeria_69_wilayas/communes.json`

## 🎯 Use It For

- E-commerce checkout forms (wilaya → commune dropdowns)
- Delivery apps and shipping integrations
- Maps and location apps
- Data visualization and research
- Educational projects

## 📝 Changelog

### v2.0.0 (July 2026) — ⚠️ Breaking

- **Fixed wilaya ids to match the official numbering.** Previous versions had wrong ids for 52–57 (2019 wilayas) and 60–69 (2025 wilayas). Now: 52 Béni Abbès, 53 In Salah, 54 In Guezzam, 55 Touggourt, 56 Djanet, 57 El M'Ghair, and 59–69 per Loi 26-06 (see table above). If you stored old ids, remap them.
- **Added `communes.json`** — all 1,541 communes with Arabic names and dairas.
- Added `region` for all 69 wilayas and `commune_count` per wilaya.
- Added `coastal` flag for the 14 coastal wilayas.
- Fixed El Aricha data (it split from Tlemcen, not Béchar): coordinates, elevation, phone/postal codes.
- Corrected spellings: Timimoun, Aïn Oussera.

### v1.1.0 (November 2025)

- Added the 11 new wilayas (59–69).

## 📝 License

MIT License - Free to use for anything!

## 🤝 Want to Help?

Found an error? Want to add more info (populations, postal codes for the newer wilayas)? Just open an issue or pull request!

## ⭐ Support

If this helped you, give it a star! ⭐

---

**Made for Algeria** 🇩🇿 | Last updated: July 2026
