> `Changelog:`
> - All significant changes to this project will be documented here.
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
> - Changed `GOBLOK` main menu with `[0]` Help and `[x]` Exit options.
> - Changed `cp` in `GOBLOK` with `2>/dev/null` to suppress same-file warning.
> - Fixed `NAME_MODULE` undefined in `post_install_actions` in `customize.sh`.
> - Fixed `BLOCKED_COUNT` recalculated on every menu iteration in `GOBLOK`.
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