# Updating the Minecraft Version of the server

Note to self: upstairs wifi

```# SSH to the server as yourself
su
su minecraftadmin
cd```

The world files are in the `world` subdirectory, including applicable mods.

```sudo java -jar fabric-installer-1.1.0.jar server -downloadMinecraft -mcversion 26.1.1
```



```
cd world/datapacks

cd ~/downloads
wget https://cdn.modrinth.com/data/1u6JkXh5/versions/DjiTrN5B/worldedit-mod-7.4.3-beta-01.jar
wget https://cdn.modrinth.com/data/VoVJ47kN/versions/mBNoWFjz/BlazeandCave%27s%20Advancements%20Pack%201.20.3.zip
wget https://cdn.modrinth.com/data/Qx9yFN48/versions/vC7sueAH/BACAP_Enhanced_Discoveries_2.8.1.zip

cp "BlazeandCave's Advancements Pack 1.20.3.zip" ~/world/datapacks
cp BACAP_Enhanced_Discoveries_2.8.1.zip ~/world/datapacks
cp "BlazeandCave's Advancements Pack 1.20.3.zip" ~/world_design/datapacks
cp worldedit-mod-7.4.3-beta-01.jar ~/mods
```

Bring up the server to test.

```sudo java -Xmx8G -Xms8G -jar fabric-server-launch.jar nogui```