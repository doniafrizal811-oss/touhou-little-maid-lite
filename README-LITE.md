# TouhouLittleMaid - Lite Version (RAM 2GB Optimized)

**Version yang dioptimalkan untuk perangkat dengan spesifikasi rendah**

## 🎯 Fitur Lite Version

- ✅ Semua fitur utama **Touhou Little Maid** tetap ada
- ❌ **TACZ weapon mod dependency dihapus** → Hemat ~50MB
- ✅ Model dan animasi maid tetap optimal
- ✅ Kompatibel dengan Minecraft Fabric 1.20.1

## 📦 Perubahan Utama

### Yang Dihapus:
1. **TACZ Weapon Mod Integration** (Mengurangi ~50-100MB)
   - Dependency: `libs:TACZ-Refabricated-1.20.1`
   - Dependency: `maven.modrinth:modernkeybinding`
   - Weapon system features
   - Gun task untuk maid

2. **Heavy Audio Libraries** (optional):
   - Opus codec (vorbis-java-core) - dapat dioptimalkan lebih lanjut

### Yang Dipertahankan:
- ✅ Maid spawning dan interaksi
- ✅ Model/animasi karakter
- ✅ Sistem inventory maid
- ✅ Quests dan tasks (kecuali gun task)
- ✅ Customization system
- ✅ Furniture dan dekorasi
- ✅ Accessories system

## 💾 Estimasi Ukuran

| Versi | Ukuran JAR | Ukuran Dengan Dependencies |
|-------|-----------|---------------------------|
| Full | ~15MB | ~150MB+ |
| Lite | ~8-10MB | ~90-100MB |

## 🚀 Instalasi

1. Clone atau download repository ini
2. Gunakan `build.gradle` versi lite (sudah dikonfigurasi)
3. Jalankan: `./gradlew build`
4. JAR akan tersedia di `build/libs/`

## 📋 Requirements

- **Java 17+**
- **Fabric Loader 0.14+**
- **Fabric API** (sesuai versi Minecraft)
- **Minecraft 1.20.1**

### Recommended Mods:
- Forge Config API Port (required)
- Cloth Config API (untuk in-game settings)
- Sodium + Iris (untuk performance lebih baik di RAM 2GB)

## ⚙️ Konfigurasi untuk RAM Minimal

Untuk HP/PC dengan RAM 2GB, aktifkan optimization ini:

```
modOptions {
  touhou_little_maid {
    # Kurangi max entity count
    entity_render_distance = 32
    
    # Disable heavy particles
    disable_particles = true
    
    # Reduce model detail
    model_quality = "low"
    
    # Disable ambient sounds
    disable_ambient_sound = true
  }
}
```

## 🔧 Development

```bash
# Clone
git clone https://github.com/doniafrizal811-oss/touhou-little-maid-lite.git

# Setup
./gradlew genSources

# Build
./gradlew build

# Run (debug)
./gradlew runClient
```

## 📝 Perubahan dari Versi Original

- **Commit**: Didasarkan pada versi Sh1roCu (44666d8002aad0ce592c6f607cc243c798fc4038)
- **Modifikasi**: Dependency TACZ dihapus
- **Target**: Low-end devices (RAM 2GB)

## ⚠️ Catatan Penting

- Lite version **tidak kompatibel** dengan TACZ weapon mod
- Beberapa fitur gun task akan hilang
- Performa lebih baik pada device dengan RAM terbatas
- Rekomendasi pakai Sodium + Iris untuk performa optimal

## 📞 Support

Issues? Silakan buat issue di repository ini dengan label `lite-version`.

---

**Status**: ✅ Siap digunakan  
**Last Updated**: 2026-07-26  
**Compatible with**: Minecraft 1.20.1
