# 🚀 Performance Guide - RAM 2GB Optimization

## Recommended Settings untuk RAM 2GB

### JVM Arguments (CRITICAL!)

```
-Xmx1024M -Xms512M -XX:+UseG1GC -XX:MaxGCPauseMillis=200 -XX:G1HeapRegionSize=16M
```

### Minecraft Video Settings

```
Render Distance: 6-8 chunks
Simulation Distance: 4-5 chunks
Graphics Mode: Fast
Particles: Minimal
VSync: ON (60fps cap)
Brightness: Normal
```

### Maid Config (.minecraft/config/touhou_little_maid-client.toml)

```toml
[maid]
    maid_render_distance = 16
    enable_maid_lod = true
    disable_death_particles = true
    disable_attack_particles = true
    enable_maid_sounds = true        # KEEP MAID VOICE!
    maid_voice_volume = 100
    max_render_maids = 2
    max_total_maids = 3
```

### Recommended Mods

| Mod | Purpose | Priority |
|-----|---------|----------|
| Sodium | Performance boost 2-3x | ⭐⭐⭐ CRITICAL |
| Iris | Shader support | ⭐⭐ Optional |
| Cloth Config | Settings GUI | ⭐⭐ Recommended |
| ModMenu | Mod manager | ⭐ Optional |

---

## Performance Tips

### Top 5 Tips

1. **Install Sodium** (MUST HAVE!)
2. **Low Render Distance** (6-8 chunks)
3. **Disable Particles** (keep FPS high)
4. **Monitor RAM** (keep >200MB free)
5. **Use Fast Graphics** (disable fancy rendering)

---

## Troubleshooting

### Problem: Still Lag at RAM 2GB

**Solutions:**
1. Install Sodium (CRITICAL!)
2. Reduce render distance to 4
3. Reduce max maids to 1
4. Close other apps
5. Increase JVM heap to 1024M

### Problem: Maid Voice Not Working

**Solutions:**
1. Check Minecraft volume (should be 100%)
2. Check enable_maid_sounds = true
3. Restart game
4. Check speaker/headphone

---

## Estimated Performance

| Device | RAM | CPU | FPS | Status |
|--------|-----|-----|-----|--------|
| HP (Low-End) | 2GB | Snapdragon 665 | 20-30 | ✅ Playable |
| PC (Budget) | 2GB | i3-8100 | 30-40 | ✅ Smooth |
| PC (Mid) | 4GB | i5-9400 | 60+ | ✅ Very Smooth |

---

## Memory Usage

```
Baseline Minecraft: ~500MB
Maid Mod: ~100-150MB
Optimization Overhead: ~50-100MB
Total: ~650-750MB (within 1GB limit)
```

**Fits perfectly in RAM 2GB!** ✅
