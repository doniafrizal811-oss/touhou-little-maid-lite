# Custom Maid Lite — Fabric 1.20.1

Mod companion maid ringan untuk Fabric 1.20.1.  
Cocok untuk HP RAM 2GB (Oppo A3s, dll).

---

## Fitur

| Fitur | Detail |
|---|---|
| 🎭 **Model YSM** | Taruh file `.json` model di folder config → langsung muncul di menu |
| 👶 **Gendong (Piggyback)** | Shift + Klik kanan maid → maid naik ke bahumu |
| 🪑 **Duduk / Berdiri** | Klik kanan biasa pada maid jinak |
| ⚔️ **Defend Owner** | Maid melindungi pemilik dari serangan |
| 💊 **Healing** | Beri golden carrot / golden apple untuk heal maid |
| 🏷️ **Ganti Nama** | Pakai name tag seperti biasa |
| 🌍 **Multi-bahasa** | Indonesia + English |

---

## Cara Pakai

### Penjinakan
1. Spawn maid dengan **Spawn Egg Maid** (dari tab Creative "Custom Maid")
2. Pegang gula / kue / cookie, klik kanan maid (33% chance tame)
3. Maid jinak = milik kamu

### Kontrol
- **Klik kanan** maid jinak → duduk / berdiri  
- **Shift + Klik kanan** maid jinak → **gendong / lepas gendong**
- **Tombol M** → buka menu pilih model untuk player kamu sendiri
- **Shift + Klik kanan** maid jinak sambil buka menu → ganti model maid

### Pasang Model YSM
1. Taruh file `.json` model di: `.minecraft/config/customplayermodel/models/`
2. Taruh texture di: `.minecraft/assets/customplayermodel/textures/entity/<nama_model>/`
3. Klik tombol ⟳ di menu untuk refresh daftar

**Format model yang didukung:**
- Format YSM (Yes Steve Model) `{"meta":{...}, "bones":[...]}`
- Format Bedrock Geometry `{"minecraft:geometry":[...]}`
- Format sederhana `{"name":"...", "texture":"...", "bones":[...]}`

---

## Build via GitHub Actions

1. Buat repo GitHub baru (public atau private)
2. Upload semua file mod ini ke root repo
3. Buka tab **Actions** → pilih **Build Custom Maid Lite JAR**
4. Klik **Run workflow**
5. Setelah selesai, download JAR dari tab **Artifacts**

---

## Optimasi HP RAM 2GB

- Model LRU cache max 10 (model lama otomatis dibuang dari memory)
- AI goal sederhana, cooldown 40 tick untuk wander
- Pathfinding range 16 blok saja (tidak scan jauh-jauh)
- Carry position update tiap 3 tick (bukan setiap tick)
- Tidak ada dependency berat (GeckoLib, dll)

---

## Error / Bug?

Lihat folder `logs/` di `.minecraft/logs/latest.log` dan cari `[CustomMaid]`.
