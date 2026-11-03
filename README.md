OpenCore EFI files for the HP Elite x2 G4, tested on macOS Sequoia.

It should also work with macOS Tahoe, but it may be too demanding for this hardware.

## OpCore Simplify Output

#### 1. CPU:
   - Intel(R) Core(TM) i7-8565U: Up to macOS Tahoe 26

#### 2. GPU:
   - Intel(R) UHD Graphics 620: Up to macOS Tahoe 26
     - Connected Monitor: SHP148C (Internal)

#### 3. Sound:
   - Intel(R) Display Audio: Up to macOS Tahoe 26
   - Realtek(R) Audio: Up to macOS Tahoe 26
     - Audio Endpoint: Speakers
   - Intel(R) Smart Sound Technology (Intel® SST): Up to macOS Tahoe 26
     - Audio Endpoint: Microphone Array

#### 4. Biometric:
   Note: Biometric authentication in macOS requires Apple T2 Chip,
         which is not available for Hackintosh systems.

   - Facial Recognition (Windows Hello) Software Device: Unsupported

#### 5. Network:
   - Intel(R) Wi-Fi 6 AX200 160MHz: Up to macOS Tahoe 26
     - Continuity Support: Partial (Handoff and Universal Clipboard with AirportItlwm)
     Note: AirDrop, Universal Clipboard, Instant Hotspot,... not available
   - Intel(R) XMM(TM) 7360 LTE-A: Unchecked

#### 6. Storage Controllers:
   - BG3 X2 NVMe SSD Controller (DRAM-less): Up to macOS Tahoe 26

#### 7. Bluetooth:
   - Intel(R) Wireless Bluetooth(R): Up to macOS Tahoe 26

## Working Features

1. CPU Power Management (P-States and C-States)
2. Wi-Fi (Not native; works via HeliPort: https://github.com/OpenIntelWireless/heliport)
3. Full HD Display (This was the tricky part! :))
4. Keyboard Shortcuts
5. Bluetooth
6. Trackpad (Multi-touch gestures are not supported)
7. Headphone Jack
8. Sleep Modes

## Not Working

1. Built-in Speakers
2. Fingerprint Sensor
3. Front and Rear Cameras

# Using EFI

## 1. BIOS Setting

During startup, press F10 to enter the BIOS settings.

Disable Secure Boot and Fast Boot. Also, configure the UEFI boot settings to enable Legacy Support.

## 2. USB Preparation

Using Rufus, format a USB flash drive with at least 1 GB of capacity as a Non-bootable disk & GPT.

<img width="500" alt="image" src="https://github.com/user-attachments/assets/717c0d1d-5402-4d87-87ea-12192756697d" />

Copy the EFI folder to the root directory of the USB drive. The folder structure should look like this:

<img width="236" height="308" alt="Screenshot 2026-11-03 at 18 38 15" src="https://github.com/user-attachments/assets/e47e7ca1-90d8-4582-b635-9d6b1937fb48" />

## 3. Installation

Continue with the standard macOS installation process. The system will restart several times during the installation.

