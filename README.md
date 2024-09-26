# Google Maps Packet Tracing via Wireshark
## Goal of the Project:
The main objective of this project was to track the origin and destination of data that is present on a network. 

## Tools Used: 
- Visual Studio Code
- Wireshark
- GeoLiteCity Repository (https://github.com/mbcc2006/GeoLiteCity-data)

## Methodology:
The first step towards achieving the goals stated above is to download the required libraries, which are dpkt and pygeoip, by typing “pip install [required library]” in terminal/command prompt. By typing this command it will download the libraries and any dependencies to your computer which is vital for the project to work. After downloading those the user will need to download the GeoLiteCity repository from GitHub. This repository is a database that will be used to translate an IP address into a Geolocation (longitude & latitude). After downloading this the user should open up Wireshark and let it run for 20 seconds and stop the data analysis. Then they should save that data analysis as a .pcap file in their root folder where this project is located. Once that is completed the user can start programming using python. In a file called main.py the libraries socket, dpkt, and pygeoip were imported, and then the default geolocation database was set to the GeoLiteCity.dat file that was downloaded earlier. After setting the default geolocation the tracer is then instructed to read the .pcap file and then print out the .kml file header which will be used later to interface with google maps. Then the source and destination IP addresses are parsed out of the .pcap file and added to the .kml variable. Then finally the tracer can acquire a source latitude and longitude using my public IP address and also the destination longitude and latitude. Using all of this information a .kml formatted text will be printed out which then needs to be put into a .txt file and converted to a .kml file. The .kml file now has all of the pertinent information regarding IP addresses, countries, and locations and now this file simply needs to be uploaded to MyGoogle maps. After uploading the .kml file the user can now see the location and destination of data that is traveling in their network.

# Images
<img width="1680" alt="image" src="https://github.com/user-attachments/assets/6cb7e6db-7a8e-46eb-a99e-8db61de0131d">


## Challenges Faced: 
1) One of the biggest challenges that I faced was properly downloading the geolocation database. This was because it was in a different format than I’m used to and because of that I had to learn how to adequately use it to convert public IP addresses to an actual location (country and city).

