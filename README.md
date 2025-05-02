
# 🚀 CrDroid 15 Kernel with KernelSU or KernelSU Next for OnePlus 7 / 7 Pro / 7T SM8150

**Universal Android 15 Custom Kernel**  
_Seamless support for CrDroid 15, LineageOS 22.1, and any Android 15-based ROMs!_

---

## ✨ Features

- **KernelSU Next**: Native root solution for advanced users.
- **Android 15 Ready**: Works out-of-the-box with CrDroid 15, LineageOS 22.1, and all Android 15 ROMs.
- **OnePlus 7 / 7 Pro**: Specifically tuned for OP7 and OP7 Pro devices.
- **Wi-Fi Module Included**: Bundled `wlan.ko` for easy Wi-Fi fixes.

---

## 📦 Installation

### 1. Flash with AnyKernel3 (Recommended)

- Download the `AnyKernel3` zip from [Releases](./releases).
- Flash it in your custom recovery (e.g., TWRP, OrangeFox).

### 2. Boot Directly with Fastboot

- Extract `boot.img` from the zip.
- Boot for testing:
  ```
  fastboot boot boot.img
  ```
- If it works, you can flash it permanently:
  ```
  fastboot flash boot boot.img
  ```

---

## 📶 Wi-Fi Not Working?

If Wi-Fi does **not** work after flashing:

1. Download the `wlan.ko` module from [Releases](./releases).
2. Push it to your device:
   ```
   adb push wlan.ko /data/local/tmp/
   ```
3. On your device (with root):
   ```
   su
   insmod /data/local/tmp/wlan.ko
   ```
   _You must have root access to load the module._

---

## 🗂️ Project Structure

```
.
├── AnyKernel3/                       # Flashable kernel zip
├── modules/
│   └── vendor/lib/modules/wlan.ko    # Wi-Fi kernel module
├── boot.img                          # Standalone boot image (optional)
├── README.md
```

---

## ℹ️ Notes

- Always backup your boot and data partitions before flashing custom kernels.
- For best results, use the provided AnyKernel3 zip.
- If you encounter issues, try booting with `fastboot boot boot.img` before flashing.

---

## 🤝 Credits

- [CrDroid](https://crdroid.net/)
- [KernelSU](https://github.com/tiann/KernelSU)
- [LineageOS](https://lineageos.org/)
- [osm0sis/AnyKernel3](https://github.com/osm0sis/AnyKernel3)

---

> _Enjoy a smoother, more powerful Android 15 experience on your OnePlus 7 / 7 Pro / 7T
