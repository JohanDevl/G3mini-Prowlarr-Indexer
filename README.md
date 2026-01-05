<p align="center">
  <img src="https://img.shields.io/badge/Prowlarr-Indexer-blueviolet?style=for-the-badge" alt="Prowlarr Indexer"/>
  <img src="https://img.shields.io/badge/Language-French-blue?style=for-the-badge" alt="French"/>
</p>

# G3mini - Prowlarr Indexer

Custom Prowlarr/Jackett indexer definition for **G3mini**, a French private torrent tracker for Movies, TV Shows, and General content.

---

## 📦 Installation

### Step 1 — Copy the indexer file

Download [`g3mini-api.yml`](https://github.com/JohanDevl/G3mini-Prowlarr-Indexer/blob/main/g3mini-api.yml) and copy it to Prowlarr's custom definitions folder:

| Platform | Path                                     |
| :------- | :--------------------------------------- |
| Linux    | `~/.config/Prowlarr/Definitions/Custom/` |
| Windows  | `%AppData%\Prowlarr\Definitions\Custom\` |
| Docker   | `/config/Definitions/Custom/`            |

### Step 2 — Restart Prowlarr

```bash
# Docker
docker restart prowlarr

# Systemd
sudo systemctl restart prowlarr
```

### Step 3 — Configure the indexer

1. Go to **Indexers** → **Add Indexer**
2. Search for **"G3mini"**
3. Enter your **API Key** (found in your G3mini profile under Settings → API Key)
4. Click **Test** then **Save**

---

## ✨ Features

| Feature                                       | Status |
| :-------------------------------------------- | :----: |
| API-based (no scraping)                       |   ✅   |
| Bearer token authentication                   |   ✅   |
| Category filtering                            |   ✅   |
| Freeleech filter                              |   ✅   |
| Season/Episode search                         |   ✅   |
| IMDB/TMDB/TVDB search                         |   ✅   |
| Language tag replacement (MULTI, VFQ, VOSTFR) |   ✅   |

---

## 📂 Categories

| ID  | Category           |
| :-- | :----------------- |
| 1   | Films              |
| 6   | Films VOSTFR       |
| 2   | Series             |
| 7   | Series VOSTFR      |
| 8   | Series Pack        |
| 9   | Series Pack VOSTFR |
| 3   | Ebooks             |
| 4   | Jeux               |
| 5   | Logiciel           |
| 10  | Sports             |

---

## ⚙️ Settings

| Setting                  | Description                                                               |
| :----------------------- | :------------------------------------------------------------------------ |
| **API Key**              | Your personal API key from G3mini                                         |
| **Freeleech only**       | Filter to show only freeleech torrents                                    |
| **Single file filename** | Use filename as title for single-file releases                            |
| **Replace MULTI**        | Replace MULTI tag with specific language                                  |
| **Replace VOSTFR**       | Replace VOSTFR/SUBFRENCH with ENGLISH                                     |
| **Replace VFQ**          | Replace VFQ with FRENCH                                                   |
| **Sort by**              | Sort results (created, bumped, seeders, leechers, size, title, completed) |

---

## 🔧 Troubleshooting

**Indexer not found after restart?**

- Verify the file is in the correct `Definitions/Custom/` folder
- Check file permissions

**Authentication failed?**

- Verify your API key is correct
- Ensure your account is active on G3mini

**No results?**

- Try a broader search query
- Check if the category exists on the tracker

---

## 📜 Tracker Rules

| Rule              | Value  |
| :---------------- | :----- |
| Minimum ratio     | 0.5    |
| Minimum seed time | 3 days |

---

## 📄 License

MIT License
