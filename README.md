## Features:

* Configuration for the M400 3D printer.
  - It can be restored to its original state even if the user makes arbitrary corrections by mistake.
  - If the manufacturer updates you, you can receive the service remotely.
 
## Requirements:

* You have to define it in moonracker.cfg.
* You will also need to make sure the following is defined in `moonraker.conf`:
  
    ```yaml
    [update_manager M400_configuration]
    type: git_repo
    channel: dev
    path: ~/M400_configuration
    origin: https://github.com/MOMENT3D/M400_configuration.git
    managed_services: klipper
    primary_branch: main

    ```

## Installation:

Moonraker's Update Manager utility. This will allow you to easily install and helps to provide future updates when more features are rolled out!

* `ssh` into your Klipper device and execute the following commands:
   ```bash
    cd
    
    git clone https://github.com/MOMENT3D/M400_configuration.git
    
    ln -s ~/M400_configuration printer_data/config/M400

    ```    
