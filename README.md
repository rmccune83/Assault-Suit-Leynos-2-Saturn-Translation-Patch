# Assault Suit Leynos 2 for Sega Saturn: English translation patch

An unofficial English translation of *Assault Suit Leynos 2*, a Japanese Sega Saturn mech shooter developed by NCS (Nippon Computer Systems) and published by Masaya in 1997.

This is a fan project. It is not affiliated with NCS, Masaya, Sega or the game's rights holders. This repository contains no game files, so you need your own copy of the Japanese disc. The patch and manual are provided on the [Releases](https://github.com/rmccune83/Assault-Suit-Leynos-2-Saturn-Translation-Patch/releases) page.

The English translation is 100% complete. The game was played through fully without issue, tested on real Sega Saturn hardware as well as in emulators.

## Credits

- **Hacking:** ryanm8
- **Testing:** Danthrax
- **Tips on extracting the official script:** KoolFiller

## What you need

- Your own copy of the Japanese *Assault Suit Leynos 2* disc: the `.cue` sheet, Track 01 and Tracks 02 to 14 (15 files in all).
- Your original Track 01 file must be named exactly `Assault Suit Leynos 2 (Japan) (Track 01).bin`, be 109,462,080 bytes, and have the SHA-256 `92b803ccbf509a913cb5de074b27cd1fb9cc380cfeb4650abc553d8f1203097e`.
- xdelta 3. Version 3.1.0 is the one tested.
- The patch file `Assault Suit Leynos 2 (Japan) (Track 01) [T-En v1.0].xdelta` (2,589,863 bytes, SHA-256 `2cc12fcc3dcf5a04e91543c3d8b9be7ab26f48a0b3e73f2263b19f1844b4205c`), from the [latest release](https://github.com/rmccune83/Assault-Suit-Leynos-2-Saturn-Translation-Patch/releases/latest).

A game manual is included along with the patch in the release.

## Applying the patch

The patch always starts from the original Japanese Track 01. Apply it to your original file, not to a copy that has already been patched.

1. Create a new folder called `English`.
2. Run xdelta 3 from the folder that holds the patch and your Track 01 file:

   ```
   xdelta3 -d -s "Assault Suit Leynos 2 (Japan) (Track 01).bin" "Assault Suit Leynos 2 (Japan) (Track 01) [T-En v1.0].xdelta" "English\Assault Suit Leynos 2 (Japan) (Track 01).bin"
   ```

3. Copy the `.cue` file and Tracks 02 to 14 from your disc into `English`. Do not copy the original Track 01, because the patched one is already in `English`. Keep every file name as it is, because the `.cue` file names the tracks.
4. Open the `.cue` file in an emulator, or load it on your Saturn by your usual method.

If your Track 01 does not match the SHA-256 above, this patch is not for your disc. Do not apply it.

### Checking the result

The patched Track 01 should be 109,462,080 bytes with the SHA-256:

```
de161d6cb511217995caf36ccd01dae6a6285ada02be7617dd39b2997b712852
```

On Windows you can check it with:

```
certutil -hashfile "English\Assault Suit Leynos 2 (Japan) (Track 01).bin" SHA256
```

## What is translated

The following is translated:

- All dialogue found on the disc
- The save-data screen and the disk select message
- The story texts for missions 1 to 7
- The mission title objective lines
- The opening timeline
- The pause screen help line
- The setup screens: main menu, weapon, device, armor, power setting and select body
- The title screen credit line
- The ending news bulletin

## How the translation was made

The translation was pulled from the official script in the Saturn Tribute release of Assault Suit Leynos 2.

## Reporting problems

For mistranslations, bugs or suggestions, please open an issue on this repository.

## Licence

The files in this repository are under the MIT Licence (see [LICENSE](LICENSE)). That licence gives no rights in *Assault Suit Leynos 2*. The game belongs to its copyright holders.
