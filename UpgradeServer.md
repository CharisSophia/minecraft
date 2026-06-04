# Updating the Minecraft Version of the server

```
# SSH to the server as yourself
su
su minecraftadmin
cd
```

The world files are in the `world` subdirectory, including applicable mods.

```
sudo java -jar fabric-installer-1.1.0.jar server -downloadMinecraft -mcversion 26.1.1
```



```
# ----------
# what needs updating?
# ----------
ls -1 mods/
ls -1 world*/datapacks/

# mods/
#  fabric-api-0.146.1+26.1.2.jar
#  mob-heads-v4.6.4.jar
#  worldedit-mod-7.4.3-beta-01.jar
# 
# world_bac/datapacks:
#  BACAP_Enhanced_Discoveries_2.8.1.zip
# "BlazeandCave's Advancements Pack 1.20.3.zip"
#  VanillaTweaks_d749145_UNZIP_ME.zip
# 
# world/datapacks:
# "BlazeandCave's Advancements Pack 1.20.3.zip"
# 
# world_design/datapacks:
# "BlazeandCave's Advancements Pack 1.20.3.zip"

# ----------
# get files
# ----------
cd ~/downloads

wget https://cdn.modrinth.com/data/1u6JkXh5/versions/DjiTrN5B/worldedit-mod-7.4.3-beta-01.jar
wget https://cdn.modrinth.com/data/VoVJ47kN/versions/mBNoWFjz/BlazeandCave%27s%20Advancements%20Pack%201.20.3.zip
wget https://cdn.modrinth.com/data/Qx9yFN48/versions/GMRG3QsC/BACAP_Enhanced_Discoveries_2.8.2.zip
wget https://cdn.modrinth.com/data/82uI0waE/versions/kZI9C6BF/mob-heads-v4.6.4.jar
wget https://cdn.modrinth.com/data/P7dR8mSH/versions/E1mjhYMF/fabric-api-0.150.0%2B26.1.2.jar

# ----------
# mods
# ----------
rm ../mods/*

cp fabric-ap* ~/mods/
cp worldedit* ~/mods/
cp mob-heads* ~/mods/

# ----------
# datapacks
# ----------
rm ../world*/datapacks/*     # clear out the old ones

cp BACAP_Enhan* ../world_bac/datapacks/
cp BlazeandCave* ../world/datapacks/
cp BlazeandCave* ../world_bac/datapacks/
cp BlazeandCave* ../world_design/datapacks/

# ----------
# verify
# ----------
ls -1 ../mods/
ls -1 ../world*/datapacks/


# ../mods/
#  fabric-api-0.150.0+26.1.2.jar
#  mob-heads-v4.6.4.jar
#  worldedit-mod-7.4.3-beta-01.jar
# 
# ../world_bac/datapacks/:
#  BACAP_Enhanced_Discoveries_2.8.2.zip
#  "BlazeandCave's Advancements Pack 1.20.3.zip"
# 
# ../world/datapacks/:
#  "BlazeandCave's Advancements Pack 1.20.3.zip"
# 
# ../world_design/datapacks/:
#  "BlazeandCave's Advancements Pack 1.20.3.zip"
```

Bring up the server to test.

```sudo java -Xmx8G -Xms8G -jar fabric-server-launch.jar nogui```
