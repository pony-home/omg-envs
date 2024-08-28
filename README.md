PlatformIO environment configs for the OpenMQTTGateway
======================================================

Usage
-----

Recommended way is to create symlinks in the OpenMQTTGateway repo dir pointing to each individual env config file located in this repo.

Optionally you can create `secret_env.ini` (ignored by the Git) taking [secret_env.ini.example](./secret_env.ini.example) as an example and populating it with relevant values. This will completely disable ESP WifiManager and configure OpenMQTTGateway using variables provided in the `secret_env.ini`

Example:
```bash
cd /path/to/the/OpenMQTTGateway
ln -sf /path/to/the/omg-envs/omg_grower_env.ini .
ln -sf /path/to/the/omg-envs/omg_d1mini_rf_env.ini .
ln -sf /path/to/the/omg-envs/secret_env.ini .
```

Install [PlatformIO](https://platformio.org) for Visual Studio Code.

Open /path/to/the/OpenMQTTGateway inside VSCode

Switch to the appropriate PlatformIO env, "OTA" envs are recommended for simplicty and remote firmware uploads, however for debugging purposes you might want to connect your device via cable and use "non-OTA" env, like `d1mini-grower-prod` etc.

Now you're ready to build/upload firmware or connect to your device via serial monitor using PlatformIO inside VSCode

