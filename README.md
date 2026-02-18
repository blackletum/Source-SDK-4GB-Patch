# Source Engine 2006/2007 – 4GB (Large Address Aware) Patch

This repository provides **Large Address Aware (4GB) patched executables** for:

- Source SDK Base 2006  
- Source SDK Base 2007
- Source SDK Base 2013 Multiplayer [previous2021]
- Source SDK Base 2013 Multiplayer [default]
- Source SDK Base 2013 Singleplayer [upcoming]

These patched executables allow the engine to use up to **4GB of virtual address space** on 64‑bit Windows instead of being limited to 2GB.

---

## What This Does

The 2006, 2007, and 2013 Source engine branches were built **without** the `/LARGEADDRESSAWARE` flag enabled.

On 64‑bit Windows, that means:

- Default limit: **2GB**
- With this patch: **Up to 4GB virtual address space**

This helps reduce crashes in heavily modded environments where memory usage approaches the 2GB ceiling. It can also, in semi-rare cases, make certain mods more stable when being played.

---

## Installation

### Step 1 – Open the Install Folder from Steam

1. Open **Steam**
2. Go to your **Library**
3. Locate:
   - **Source SDK Base [whatever]**
4. Right‑click the entry
5. Click **Manage**
6. Click **Browse local files**

Steam will open the correct install directory automatically.

---

### Step 2 – Replace `hl2.exe`

1. Download the matching patched `hl2.exe` from this repository.
2. Drag it into the folder that Steam opened.
3. Allow Windows to replace the existing file.

No manual backup is required.

If anything goes wrong, Steam’s integrity check will restore the original file, detailed in the next section.

---

## Restoring the Original Executable

To revert to the official unmodified executable at any time:

1. Open **Steam**
2. Go to your **Library**
3. Right‑click the **Source SDK base 2006** or **Source SDK base 2007** 
4. Click **Properties**
5. Go to **Installed Files**
6. Click **Verify integrity of tool files**

Steam will:

- Detect the modified `hl2.exe`
- Re-download the official version
- Restore everything automatically

No manual cleanup is needed.

---

## Notes

- This does **not** convert the engine to 64‑bit.
- This does **not** increase performance.
- This only increases available virtual address space.
- Stability beyond ~3GB may still be limited due to 32‑bit memory fragmentation.
- Only effective on **64‑bit Windows**. This **may** work on 32-bit Windows, but will only allow up to 3GB of memory.
- Use at your **own risk**. Normally, it is not advisable to download EXE files from the internet. You can patch the files yourself using the same 4GB patcher available here: [NTCore 4GB Patch](https://ntcore.com/4gb-patch/)


---

## When This Is Useful

You may benefit from this patch if:

- You run large custom maps
- You use high-resolution texture packs
- You experience crashes near 1.8–2.0GB memory usage
- You are developing or testing large Source mods

---

## Disclaimer

- This patch modifies the executable header to enable Large Address Aware.  
- No engine logic or gameplay code has been changed.
- Use at your own risk.
