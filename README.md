# Stellar XboxHD+ - Upscaler Profiles
<p >
 <a href=""><img src="https://img.shields.io/discord/643467096906399804.svg" alt="Chat"></a>
 <a href="https://github.com/MakeMHz/project-stellar/issues"><img src="https://img.shields.io/github/issues/MakeMHz/project-stellar.svg" alt="GitHub Issues"></a>
 <a href=""><img src="https://img.shields.io/badge/contributions-welcome-orange.svg" alt="Contributions welcome"></a>
</p>

> stellar (adj) - exceptionally good; outstanding.

The world's most powerful add-on for the Original Xbox. StellarOS is the first completely legal re-implementation of the retail Xbox BIOS.

# RetroTink 4K
Currently, the RetroTink 4K does not support auto profile loading via SPD metadata. This feature has been requested. For now, the recommended
configuration is as follows.

![RetroTink Recommended](resources/images/retrotink_recommended.png)

| **Setting**                             | **Value**    |
|-----------------------------------------|------------- |
| **Output Mode**                         | Direct Video |
| **Disable Internal 640x480 HD Scaling** | Off          |
| **Disable Internal 10:11 PAR Scaling**  | Off          |

# PixelFX Morph
It is recommended to download the profile pack from the release page and copy to the profiles to the SD card of the PixelFX Morph.
Once copied over, you will need to enable ``Preset auto-load``.

\* All profiles are optimized for 4K.

![Morph Preset Auto load](resources/images/morph_preset_auto_load.png)

It is recommended that you set the following settings.

![Morph Recommended Settings](resources/images/morph_recommended.png)

| **Setting**                             | **Value**     |
|-----------------------------------------|-------------- |
| **Output Mode**                         | Direct Framed |
| **Disable Internal 640x480 HD Scaling** | On            |
| **Disable Internal 10:11 PAR Scaling**  | On            |

**RX Input CS**: Auto

![Morph RX Input CS Auto](resources/images/morph_rx_input_cs_auto.png)


## SPD Packet Format

```
Vendor : XboxHD+
Product: F 720x480 WP
         │ │       ││
         │ │       │└─────────► 10:11 Pixel Aspect Ratio
         │ │       └──────────► Widescreen
         │ └──────────────────► Internal Resolution
         └────────────────────► Output Mode
                                [4] 480p Upscale
                                [7] 720p Upscale
                                [D] Direct
                                [F] Direct Framed
                                [R] Retail Bypass
```
