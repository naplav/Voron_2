# Voron 2.4r2 300mm #2392 Klipper backup

![stealthburner](./Images/stealthburner.jpg)

![v2.4](./Images/v2.4_2392.jpg)

## Relevant Hardware
  BTT Octopus v1.1

  BTT EBB36 v1.2

  BTT U2C Can to USB Adapter v1.1

  BTT PITFT 50 v2.0

  KlickyProbe

  Pi Cam v2.0

## Installation Guide
  Install Pi OS Lite via Raspberry PI Imager in a SD Card
  Insert SD Card in your Pi
  Connect to Pi via SSH then execute:

  sudo apt update
  sudo apt upgrade
  sudo apt-get install git -y
  git clone https://github.com/th33xitus/kiauh.git
  ./kiauh/kiauh.sh

  Install Klipper, Mainsail, Fluidd, Telegram Bot, etc. In Advanced -> Extra install Shell-Command

  Then build firmware (STM32F446), download it from /home/pi/klipper/output, rename file klipper.bin to firmware.bin e copy file to a SD card.

  For installing auto z for klicky probe: https://github.com/protoloft/klipper_z_calibration

  For installing auto resonance test, enable the script by exectuing: 
  chmod +x ./klipper_config/scripts/generate_resonances_graph.py
  help for troubleshooting shebang https://askubuntu.com/questions/896860/usr-bin-env-python3-r-no-such-file-or-directory


  For installing the u2c controller: https://github.com/maz0r/klipper_canbus/blob/main/controller/u2c.md
  For installing the btt36 toolboard: https://github.com/maz0r/klipper_canbus/blob/main/toolhead/ebb36-42_v1.1.md

  For configuring Telegram Bot you need to create the bot, and insert in telegram.conf TOKEN and your chat_id.

  For configuring klipper backup: https://github.com/Low-Frequency/klipper_backup_script
  
  For installing webcam (via crownest): https://github.com/mainsail-crew/moonraker-timelapse

  For installing timelapse: https://github.com/mainsail-crew/moonraker-timelapse


