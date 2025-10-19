## JamesDSPManager

Integrate JamesDSP by following these two steps:

1.  **Build System:** Add the config to **`device.mk`**:

    ```makefile
    $(call inherit-product, packages/apps/JamesDSPManager/config.mk)
    ```

2.  **Audio Registration:** Add these lines **inside the `<libraries>` block** of **`audio_effects.xml`** (`/vendor/etc/` or `/etc/`):

    ```xml
    <library name="jdsp" path="libjamesdsp.so"/>
    <effect name="jamesdsp" library="jdsp" uuid="f27317f4-c984-4de6-9a90-545759495bf2"/>
    ```
