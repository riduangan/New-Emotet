# New-Emotet
New Emotet


With the new Emotet campaign it arrives with a new Wi-Fi Spreader module downloads to the system C:\ProgramData. The downloaded binary contains a self-extracting RAR that has two (service.exe and worm.exe) binaries to spread the infection through WiFi.

The worm.exe is the executable used for spreading the malware, once it executed it copies the service.exe to a variable for using it while spreading.

Then it calls wlanAPI.dll class that used by Native Wi-Fi to manage the wireless network profiles and connections for spreading the infection to other networks.


“The Worm enumerates all Wi-Fi devices currently enabled on the local computer, which it returns in a series of structures. These structures contain all the information relating to the Wi-Fi device, including the device’s GUID and description,” read the Binary Defense analysis.

It gathers possible information from every available Wi-Fi network present in the list of networks.




IOC:
9.file      865cf5724137fa74bd34dd1928459110385af65ffa63b3734e18d09065c0fb36

Worm.exe    077eadce8fa6fc925b3f9bdab5940c14c20d9ce50d8a2f0be08f3071ea493de8     

Service.exe 64909f9f44b02b6a4620cdb177373abb229624f34f402335ecdb4d7c8b58520b
