My changes:
* width for button background is set to 40%(in 'CSS.h'), so the whole text is on blue background on phone browser
* the file will be open as read(in 'ESP_file_download_from_SPIFFS.ino'); before the file was open for write
* the Download button is now shown on webpage(changes made in 'ESP_file_download_from_SPIFFS.ino'); before it did not show up on webpage
* it shows the list of all files that are on ESP8266(SPIFFS); changes made in 'ESP_file_download_from_SPIFFS.ino'
* this was tested only on ESP8266; i don't have any ESP32 to test it

# ESP32-8266-File-Download
Using HTTP and an HTML interface to download files from an ESP32/ESP8266

1. Download all files to a sketch folder.

2. Edit the Network tab and add in your SSID and PASSWORD, more if you have them.

3. Choose your IP address, currently it is fixed to 192.168.0.150

4. You can edit the logical name 'fileserver' to your requirements then access the device with http://fileserver.local but only if your browser has mDNS support otherwise use http://192.168.0.150/

5. NOTE: the Directory command is not included in this release, this comes later.

6. To test the download place a known file on the SD-Card for trial purposes.

NOTES:

The ESP32 is not reliable when using SD Cards, please ensure you know how to connect the SPI bus to the SD-Card if not using an MH-ET Live ESP32 board and a Wemos SD-Card Shield. Although pull-ups are enabled, you may need to add an external 4k7 pull-up too on the MISO line.

