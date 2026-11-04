# malbec

OpenHarmony product configuration for `device/board/lenovo/malbec`. Inherits
`vendor/opendroid/common` and installs product parameters.

The product selects the native Qualcomm buffer allocator, Turnip with the KGSL
kernel interface, and Mesa EGL/GLES. Keep `device/soc/qualcomm/common` and its
matching Mesa, Surface and graphics sources together. The native vendor VDI
replaces the generic buffer provider; display composition requires a separate
compatible provider.

Build host tools and native SDK requirements are documented in
`device/soc/qualcomm/common/README.md`. Host tool and existing Mesa build-cache
paths can be supplied through that component's GN arguments; this product does
not embed machine-specific paths.
