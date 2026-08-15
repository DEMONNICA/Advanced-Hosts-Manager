> `Changelog:`
> - All significant changes to this project will be documented here.
---

> [3.5.0]
>
> - Added `WHITELIST_FILE` and `CONFIG_FILE` variables in `GOBLOK`.
> - Added IP configuration loading from `CONFIG_FILE` with IPv4, IPv6, and IPv6-enabled defaults in `GOBLOK`.
> - Added `save_config` function in `GOBLOK` for persistent IP settings storage.
> - Added `hr`, `header`, `ok`, `fail`, `warn`, `kv`, and `pause` helper functions in `GOBLOK` for consistent output formatting.
> - Added `count_urls` function in `GOBLOK` for POSIX-compatible URL list counting.
> - Added `apply_whitelist` function in `GOBLOK` to filter whitelisted domains from block list.
> - Added User-Agent string to `download_url` requests in `GOBLOK`.
> - Added retry logic with backoff to `download_url` for curl, wget, and busybox wget in `GOBLOK`.
> - Added connection and timeout limits to `download_url` for curl, wget, and busybox wget in `GOBLOK`.
> - Added 1-second delay between source downloads in `GOBLOK`.
> - Added judol-guard blocklist URL to built-in sources in `GOBLOK`.
> - Added bare domain format support in `GOBLOK` `process_pipeline` for automatic IP prefix injection.
> - Added option `[4]` Remove Custom Source in `GOBLOK`, replacing the removal-less built-in/custom source view.
> - Added option `[5]` Block Domain Manually with loop input and domain validation in `GOBLOK`.
> - Added option `[6]` Whitelist Manager with add and remove support in `GOBLOK`.
> - Added option `[7]` IP Settings for IPv4, IPv6 address, and IPv6 enable/disable with automatic rebuild in `GOBLOK`.
> - Added `check_connection` function in `GOBLOK` for a fast pre-flight connectivity check before downloading sources.
> - Added `MODULE_HOSTS` initialization with header and signature in `GOBLOK` option `[5]` when the file does not yet exist.
> - Added `read < /dev/tty` for all user input in `GOBLOK` to prevent stdin consumption.
> - Added a cancel hint to the URL prompt in `GOBLOK` option `[3]`.
> - Changed `HOSTS_URLS` in `GOBLOK` from bash array to POSIX-compatible newline-separated string.
> - Changed `process_pipeline` default-entry filtering in `GOBLOK` from chained grep to a single awk script.
> - Changed `process_pipeline` dual-stack entry generation in `GOBLOK` from a while-read loop to an awk one-liner.
> - Changed `clear` command in `GOBLOK` to an ANSI escape sequence for full screen and scrollback clear.
> - Changed menu and status output in `GOBLOK` to use the new helper functions instead of manual `printf` blocks.
> - Changed `count_real_blocked_entries` in `GOBLOK` to use a local variable preventing double output.
> - Changed `count_real_blocked_entries` in `service.sh` to use a local variable and include `::` in the pattern.
> - Changed separator in `service.sh` description from `•` to `|`.
> - Changed duplicate and removal checks in `GOBLOK` from substring match (`grep -F`) to exact-line match (`grep -xF`) in options `[4]`, `[5]`, `[6]`, and `apply_whitelist`.
> - Changed `apply_whitelist` domain filtering in `GOBLOK` from `grep` pattern matching to `awk` exact-field matching.
> - Changed `download_url` retry count and timeouts in `GOBLOK` from 3×60s to 2×20s for curl, and 3×15s to 2×10s for wget, to fail faster on dead sources.
> - Changed `update_blocked_count` in `GOBLOK` to update the blocked count only without overwriting the rest of the description.
> - Changed `GOBLOK` menu from 3 options with submenu to 7 flat options.
> - Changed `[1] Update Hosts from Default Sources` in `GOBLOK` to `[1] Apply Module Block List`.
> - Changed `[2-3] Rebuild from All Sources` submenu item in `GOBLOK` to top-level option `[2] Sync & Refresh All Sources`.
> - Changed `[2-1] Add Custom Source URL` submenu item in `GOBLOK` to top-level option `[3] Add Custom Source`, now rebuilding from all sources immediately instead of saving to a pending list.
> - Changed `mktemp` in `GOBLOK` to a direct path to fix Android compatibility.
> - Changed `[0] Back` and `[0] Cancel` labels in `GOBLOK` submenus to `[x]` for consistency with the main menu exit key.
> - Changed `customize.sh` ksud-output fallback to only distinguish `KernelSU-Next Spoofed`, `Wild KSU Spoofed`, and generic `KernelSU Spoofed`, removing the `VortexSU`/`ReSukiSU`/`SukiSU`-specific branches.
> - Fixed `BLOCKED_COUNT` recalculated on every menu iteration in `GOBLOK`.
> - Fixed separator and menu item merged in one `printf` in `GOBLOK`.
> - Fixed `0` fallback printed twice to screen in `GOBLOK`.
> - Fixed case pattern overlap in `customize.sh` ksud-output fallback causing SukiSU and ReSukiSU builds to be mislabeled as `VortexSU Spoofed`.
> - Removed root method detection block from `GOBLOK`.
> - Removed `NEW_CUSTOM_URLS_FILE` variable and its usages from `GOBLOK` as leftover from the old pending-sources workflow.
> - Removed the redundant `apply_whitelist` pass that wrote directly to `$MODULE_HOSTS` in `GOBLOK`, since the file is always rebuilt from `$DUALSTACK_FILE` immediately after.
> - Removed Termux curl path fallback (`/data/data/com.termux/files/usr/bin/curl`) from `download_url` in `GOBLOK`.
> - Removed root method display from `GOBLOK` main menu header.
> - Removed Help & Usage Guide option from `GOBLOK` main menu.
> - Removed `exec /system/bin/GOBLOK` from `service.sh`.
> - Removed `.method` file cleanup for all root manager directories from `uninstall.sh`.
---

> [2.5.0]
>
> - Added `detect_root_all` in `customize.sh` with comprehensive root detection for all supported variants.
> - Added `VortexSU` and `Kokoro Mask` detection in `customize.sh`.
> - Added aapt-based spoofed build fallback in `customize.sh`.
> - Added `set_donate_link` in `customize.sh` for timezone-based donation URL.
> - Added `verify_module_id` in `verify.sh` for module identity verification.
> - Added boot wait loop in `service.sh` before launching `GOBLOK`.
> - Added `restorecon` and `chmod` to mount block in `post-fs-data.sh`.
> - Added `.method` file cleanup in `uninstall.sh` for all root manager directories.
> - Added fstrim in `uninstall.sh` across available partitions.
> - Added `sync` before module directory removal in `uninstall.sh`.
> - Added `process_pipeline` function in `GOBLOK` for reusable filter-normalize-dualstack pipeline.
> - Added Help & Usage Guide option in `GOBLOK` main menu.
> - Added root method and version display in `GOBLOK` main menu.
> - Added `restorecon` after hosts file copy in `GOBLOK`.
> - Changed `customize.sh` root detection order to APatch → KernelSU → Magisk.
> - Changed APatch `.method` format in `customize.sh` to 5 lines including app version.
> - Changed `service.sh` root detection order to APatch → KernelSU → Magisk.
> - Changed APatch `.method` reading in `service.sh` to include `APATCH_APP_VER` on line 3.
> - Changed `GOBLOK` root detection order to APatch → KernelSU → Magisk.
> - Changed APatch `.method` reading in `GOBLOK` to include `APATCH_APP_VER` on line 3.
> - Changed `[x]` exit option in `GOBLOK` to accept both `x` and `X` input.
> - Changed `customize.sh` root detection to loop-based variant matching.
> - Changed `customize.sh` device information display into unified `device_info` function.
> - Changed `customize.sh` Android codename labels to square bracket format.
> - Changed `customize.sh` devil message display to name-only format.
> - Changed APatch version code reading in `customize.sh`.
> - Changed `icon` in `customize.sh` to extract `AHM.jpg` only.
> - Changed `verify_module` success message in `customize.sh`.
> - Changed `verify.sh` `extract` with extended hash algorithm support.
> - Changed error messages in `verify.sh` `extract` to simplified format.
> - Changed `service.sh` with `.method` file-based root detection.
> - Changed `service.sh` description to display blocked hosts count.
> - Changed `MODDIR` definition in `uninstall.sh`.
> - Changed cache cleanup in `uninstall.sh` with unified find-based approach.
> - Changed mount command in `post-fs-data.sh` with `2>/dev/null`.
> - Changed `GOBLOK` shebang to `#!/system/bin/sh`.
> - Changed `GOBLOK` path variables to top-level declarations.
> - Changed `update_blocked_count` in `GOBLOK` to update `description=` field.
> - Changed `notify_status` in `GOBLOK` to use temp file for notification delivery.
> - Changed `cp` in `GOBLOK` with `2>/dev/null` to suppress same-file warning.
> - Changed banner image in `README.md` and `module.prop`.
> - Changed license from GNU General Public License to Apache License 2.0.
> - Fixed `NAME_MODULE` undefined in `post_install_actions` in `customize.sh`.
> - Fixed stdin consumption from `| while read` pipeline in `GOBLOK`.
> - Removed `AHM01.png` and `AHM02.png` extraction from `customize.sh` and cleanup from `uninstall.sh`.
> - Removed `display_current_time`, `root_detect`, `display_device_info`, `display_ram_info`, and `check_android_version` from `customize.sh`.
> - Removed fallback `MODPATH` and `TMPDIR` declarations from `customize.sh`.
> - Removed `SKIPUNZIP` and `DEBUG` flags from `customize.sh`.
> - Removed `ARCH` variable from `customize.sh`.
> - Removed `-i` and `-I` icon flags from `GOBLOK` notification.
> - Removed feature description section from `GOBLOK` main menu.
> - Removed `MODULENAME` variable from `notify_status` in `GOBLOK`.
> - Removed dependency check from `verify.sh`.
> - Removed `zip` path cleaning from `extract` in `verify.sh`.
> - Removed version and name field updates from `service.sh`.
> - Removed Android version and emoji from `service.sh` description.
> - Removed `renice` and `ionice` from `service.sh`.
> - Removed shader cache cleanup from `uninstall.sh`.
---

> [1.0.0]
>
> - Initial release.
---