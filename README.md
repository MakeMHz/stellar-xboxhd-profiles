<img src="resources/images/logo.png" align="right" />

# Stellar XboxHD+ - Upscaler Profiles
<p >
 <a href=""><img src="https://img.shields.io/discord/643467096906399804.svg" alt="Chat"></a>
 <a href="https://github.com/MakeMHz/project-stellar/issues"><img src="https://img.shields.io/github/issues/MakeMHz/project-stellar.svg" alt="GitHub Issues"></a>
 <a href=""><img src="https://img.shields.io/badge/contributions-welcome-orange.svg" alt="Contributions welcome"></a>
</p>

> stellar (adj) - exceptionally good; outstanding.

The world's most powerful add-on for the Original Xbox. StellarOS is the first completely legal re-implementation of the retail Xbox BIOS.

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
