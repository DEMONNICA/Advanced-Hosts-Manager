> <img width="3264" height="1836" alt="Image" src="https://github.com/user-attachments/assets/84c9883a-2561-4743-80e9-e620287a64e2" />

> [!NOTE]
> ```
> Advanced system-level hosts management with real-time ad blocking, privacy protection, and automatic updates from trusted sources.
> ```

> [!IMPORTANT]
> Features ✨:
> 1. System-wide Ad Blocking replacing the system hosts file at `/system/etc/hosts` to block ads across all apps and browsers at the network level without requiring any additional app.
> 2. Privacy & Tracker Protection blocking known tracking and analytics domains to prevent data collection and protect user privacy across all network traffic.
> 3. Malware & Phishing Domain Filtering blocking domains associated with malware distribution, phishing attempts, and coin mining to keep the device secure.
> 4. Automatic Updates from Trusted Sources downloading hosts lists from multiple built-in curated sources including FadeMind extras, GoodbyeAds, and CoinBlocker with a single command.
> 5. Smart Filtering & Normalization automatically filtering comments, blank lines, and default system entries, then normalizing all addresses to `0.0.0.0` for consistent blocking.
> 6. Dual-Stack IPv4/IPv6 Support generating both `0.0.0.0` and `::1` entries for every blocked domain, ensuring complete blocking on devices with IPv6 connectivity.
> 7. Custom Hosts Sources Integration allowing registration of custom hosts list URLs with support for applying pending sources only or rebuilding from all sources at once.
> 8. Real-time Blocking Statistics displaying live blocked domain count in the root manager description and main menu, updated automatically after each successful update.
> 9. Help & Usage Guide providing a built-in detailed guide accessible directly from the main menu explaining all options and usage instructions.

> [!TIP]
> 1. Supports `Magisk` `KernelSU` `KernelSU Next` `APatch` `SukiSU` and their variants.
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
> Disclaimers 🛡️:
> - Use at your own risk. No guarantees are made regarding stability, compatibility, or safety. Always back up your data before installing anything.
> - This module is tested on specific devices only. Behavior on other devices may vary significantly.
> - The author reserves the right to discontinue, modify, or remove this module at any time without prior notice.

> [!CAUTION]
> Warning ☢️:
> 1. The developer takes no responsibility for any damage, data loss, or device malfunction caused by the use of this module.
> 2. System modifications can be unpredictable. What works on one device may break another.
> 3. Always have a recovery solution ready — TWRP, ADB, or fastboot — before proceeding.
> 4. If you do not fully understand what a modification does, do not apply it.
> 5. Redistribution, modification, or repackaging of this module without explicit permission from the author is strictly prohibited.
> 6. Rooted devices with custom ROM may behave differently. Proceed with extra caution.
> 7. Any modification applied to the system is your decision. Think before you act.