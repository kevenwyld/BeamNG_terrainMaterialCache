# BeamNG_terrainMaterialCache
Cached Texture files for BeamNG
[!](https://img.shields.io/badge/dynamic/json?label=Downloads&query=download_count&url=https%3A%2F%2Fapi.github.com%2Frepos%2FSnoutBug%2FBeamNG_terrainMaterialCache%2Freleases%2Fassets%2F52289435) 
Hack to fix the Black Terrain found after the 0.24 release on Linux

Still looking for a proper solution

Massive thanks to Bauer33333 for providing the pre-generated textures for this transplant.

## Usage (Steam - Proton)
### Default Maps
Please verify that this path exists BEFORE using the commands below

```Bash
~/.steam/root/steamapps/compatdata/284160/pfx/drive_c/users/steamuser/AppData/Local/BeamNG.drive/0.24/temp/art
```

```Bash
mkdir ~/.steam/root/steamapps/compatdata/284160/pfx/drive_c/users/steamuser/AppData/Local/BeamNG.drive/0.24/temp/art
cd "$_"
url=github.com/SnoutBug/BeamNG_terrainMaterialCache/releases/download/default/
wget ${url}etk.tar.gz
wget ${url}jri.tar.gz
wget ${url}utah.tar.gz
wget ${url}derby.tar.gz
wget ${url}hirochi.tar.gz
wget ${url}industrial.tar.gz
wget ${url}gridmap_v2.tar.gz
wget ${url}small_island.tar.gz
ls *.tar.gz | xargs -n 1 tar -xvf
rm *.tar.gz
cd ~/
```
### BeamNG Repository (Mods)
 1. Look at the URL of your map (eg. www.beamng.com/resources/natural-playground.18030/)
 2. Copy the number behind the period (18030) to the following URL like this: www.github.com/SnoutBug/BeamNG_terrainMaterialCache/releases/tag/18030
 3. If the page exists, you will find a one-liner in the release's description which you can then use to downlad the textures

### Troubleshooting
 #### The above mentioned path did not exist
 1. Open your Steam Library and find BeamNG.drive
 2. Right Click > Manage > Browse Local Files
 3. Right Click > Open Terminal (or find a different way to do so)
 4. Use the following command
```Bash
mkdir ../../compatdata/284160/pfx/drive_c/users/steamuser/AppData/Local/BeamNG.drive/0.24/temp/art
```
 5. If successful: Copy the all commands from [above](https://github.com/SnoutBug/BeamNG_terrainMaterialCache#default-maps) (**excluding** the first one)
 
 #### Running the Game with WINE
 1. Find the equivalent of: `%localappdata%\BeamNG.drive\0.24\temp\art\terrainMaterialCache`
 2. Modify the command below if need be
 ```Bash
 mkdir ~/.wine/drive_c/users/$USER/AppData/Local/BeamNG.drive/0.24/temp/art
 ```
 4. If successful: Copy the all commands from [above](https://github.com/SnoutBug/BeamNG_terrainMaterialCache#default-maps) (**excluding** the first one)

## Contribute
### You created a map using a PBR terrain and want to contribute
 1. Delete all files in `%localappdata%\BeamNG.drive\0.24\temp\art\terrainMaterialCache`
 2. Load up your map and only your map
 3. Copy all files inside of `%localappdata%\BeamNG.drive\0.24\temp\art\terrainMaterialCache` into an archive
 4. Upload the archive
 5. Use this [link](https://github.com/SnoutBug/BeamNG_terrainMaterialCache/issues/new?assignees=&labels=enhancement&template=contribute.md&title=Repository-PBR-Textures) for further steps
