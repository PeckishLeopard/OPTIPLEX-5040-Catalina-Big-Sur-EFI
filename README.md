# OPTIPLEX5040
Dell Optiplex 5040 Big Sur EFI Folder

This EFI folder has only ever been used to Install OSX Catalina, however once installed it is possible to upgrade to Big Sur with no subsequent changes. I suspect installing Big Sur from the get go will also work however this is yet to be tested.
----------------------------------
Notes for post install:

Once OS has successfully installed and the content of the UEFI partition of your USB has been coped to your Optiplex's HDD/SSD several changes listed below should be made to the config.plist file to ensure a much smoother boot experience. These both require editing the config.plist and involve disabling verbose and disabling the OpenCore picker within the boot process.

--> Disable verbose: <--
edit config.plist
Under: NVRAM > 7C436110-AB2A-4BBB-A880-FE41995C9F82 > boot-args
change: "-v keepsyms=1 debug=0x100 alcid=3" to "keepsyms=1 debug=0x100 alcid=3"

--> Disable picker: <--
edit config.plist 
Under: Misc > Boot > ShowPicker
change "YES" to "NO"

