# minecraft
Functions, command blocks, and custom achievements for Minecraft vanilla server.

To launch the server:
`java -Xmx8G -Xms8G -jar fabric-server-launch.jar nogui`

Once the Minecraft server is running, from the console, run the following commands:
```
/op CharisSophia
/gamerule doDaylightCycle false
/gamerule doFireTick false
/gamerule doMobSpawning false
/gamerule doWeatherCycle false
/time set noon
```

To update the server to the lastest Minecraft version:
`sudo java -jar fabric-installer-1.1.0.jar server -downloadMinecraft`
