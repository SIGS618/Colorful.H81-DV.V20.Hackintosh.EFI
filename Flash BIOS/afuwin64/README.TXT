AFU (AMI Firmware Update) is a package of utilities used 
to update the system BIOS under various operating systems.  

Note: AFU only works for APTIO with SMI FLASH support.
      Compatible with Aptio 3, 4, and 4.5.

The package includes:

- AFUWIN64 2.36
- AFUWINGUI 1.13
- AFUWIN Release Notes
- AFU User Guide

To run, extract all of the files from the folder with the name corresponding to the desired operating system.


Usage (applies to AFUWIN, AFUDOS, AFUEFI and AFUEFI64...
       for usage of AFUBSD and AFULNX see help files provided in their folders):
------------------------------------------------------------------
AFUDOS <BIOS ROM File Name> [Option 1] [Option 2]
Or
AFUDOS <Input or Output File Name> <Command>
Or
AFUDOS <Command>

BIOS ROM File Name
The mandatory field is used to specify path/filename of the BIOS ROM file with extension.

Commands
The mandatory field is used to select an operation mode.
- /O	Save current ROM image to file
- /U	Get and display ROM ID from BIOS ROM file
- /S	Refer to Option: /S
- /D	Verification test of given ROM File without flashing BIOS.
- /A	Refer to Option: /A
- /CLNEVNLOG 	Refer to Option: /CLNEVNLOG

Options
The optional field used to supply more information for flashing BIOS ROM. Following lists the supported optional parameters and format:
- /P	Program main bios image
- /B	Program Boot Block
- /N	Program NVRAM 	
- /E	Program Embedded Controller block if present
- /K	Program all non-critical blocks and ROM Holes
- /Kn	Program n'th non-critical block or ROM Hole only (0>= n <=7)
- /Q	Quiet mode enable
- /REBOOT	Reboot after update BIOS done
- /X	Do not check ROM ID
- /S	Display current system's BIOS ROM ID
- /R	Preserve all SMBIOS structures during programming.
- /Rn	Preserve SMBIOS type N during programming.
- /ECUF	Update EC BIOS when newer version is detected.
- /Shutdown Shutdown after programming.
- /HOLE: Upate sepcific ROM Hole according to RomHole GUID.
- /HOLEOUT: Save specific ROM Hole according to given GUID.
- /SP 	Preserve Setup setting.
- /EC	Program Embedded Controller Block.(Flash Type)
- /MEUF	Program ME Ignition Firmware Block.
- /ME	Program ME Entire Firmware Block.(only support DOS and WinPE platform)
- /CAF  Compare ROM file's data with Systems is different or not, if not then cancel related update.
- /A	Oem Activation file.
- /CLNEVNLOG 	Clear Event Log.

Rules
- Any parameter encolsed by < > is a mandatory field.
- Any parameter enclosed by [ ] is an optional field.
- <Commands> cannot co-exist with any [Options].
- Main BIOS image is default flashing area if no any option present.
- [/REBOOT], [/X], and [/S] will enable [/P] function automatically.
- If [/B] present alone, there is only the Boot Block area to be updated.
- If [/N] present alone, there is only the NVRAM area to be updated.
- If [/E] present alone, there is only the Embedded Controller block to be updated.
