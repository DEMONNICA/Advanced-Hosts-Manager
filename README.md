> <img width="3264" height="1836" alt="Image" src="https://github.com/user-attachments/assets/84c9883a-2561-4743-80e9-e620287a64e2" />

> [!NOTE]
> ```
> Advanced system-level hosts management with real-time ad blocking, privacy protection, and automatic updates from trusted sources.
> ```

> [!IMPORTANT]
> Features ✨:
> 1. System-wide Ad Blocking at the network level via `/system/etc/hosts` — works across all apps and browsers, no extra app needed.
> 2. Privacy & Tracker Protection by blocking known tracking and analytics domains.
> 3. Malware & Phishing Filtering to keep the device secure from unsafe domains.
> 4. Automatic Updates from trusted built-in sources including FadeMind, GoodbyeAds, CoinBlocker, and Judol Guard.
> 5. Smart Filtering & Normalization that cleans and standardizes every source into a consistent block list.
> 6. Configurable Dual-Stack IPv4/IPv6 with your own blocking addresses, and the option to disable IPv6.
> 7. Custom Hosts Source Management to add, remove, and rebuild your own sources anytime.
> 8. Manual Domain Blocking to instantly block individual domains without a full rebuild.
> 9. Whitelist Manager to exclude specific domains from the block list.
> 10. Real-time Blocking Statistics shown live in the root manager description and main menu.

> [!TIP]
> 1. Supports `APatch` `KernelSU` `Magisk` and their forks.
> 2. Minimum Android `10 SDK 29`.
> 3. To run the module, open **Termux** and follow the steps below:
>    - **Method 1** — Enter root shell first, then launch the tool:
>      ```sh
>      su
>      ```
>      After pressing **Enter**, your prompt will change to `#`, meaning you are now in root mode. Then type:
>      ```sh
>      GOBLOK
>      ```
>      Press **Enter** to launch the hosts management menu.
>    - **Method 2** — Run directly in a single command:
>      ```sh
>      su -c GOBLOK
>      ```
>    > Both methods require root access. A root manager such as Magisk, KernelSU, or APatch must be installed on your device.
> 4. If `GOBLOK` command is not found, install **Meta** to enable system binary overlay support:
>    - [Download Meta — Hybrid Mount](https://github.com/Hybrid-Mount/meta-hybrid_mount/releases)
> 5. If `GOBLOK` is still not accessible after installing Meta, run it directly via full path:
>    ```sh
>    su -c /data/adb/modules/AHM/system/bin/GOBLOK
>    ```

> [!WARNING]
> 1. If you do not fully understand what a modification does, do not apply it.
> 2. Always have a recovery solution ready — TWRP, ADB, or fastboot — before proceeding.
> 3. Rooted devices with custom ROM may behave differently. Proceed with extra caution.
> 4. System modifications can be unpredictable. What works on one device may break another.
> 5. Any modification applied to the system is your decision. Think before you act.
> 6. The developer takes no responsibility for any damage, data loss, or device malfunction caused by the use of these works.
> 7. Redistribution, modification, or repackaging of these works without explicit permission from the author is strictly prohibited.

> [!CAUTION]
> Disclaimers 🛡️:
> - Use at your own risk. No guarantees are made regarding stability, compatibility, or safety. Always back up your data before installing anything.
> - These works are tested on specific devices only. Behavior on other devices may vary significantly.
> - The author reserves the right to discontinue, modify, or remove any module or plugin at any time without prior notice.