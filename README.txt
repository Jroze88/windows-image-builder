System Requirements:
====================

- Windows 7 with SP1 / Windows 8.1 / Windows 10 / Server 2008 R2 / Server 2012 R2 / Server 2016 Installation Disc DVD/ISO.
- Windows 7 with SP1 / Windows 8.1 / Windows 10 Host Operating System for Servicing Windows 7 / Windows 8.1 Source Images.
- Windows 8.1 / Windows 10 Host Operating System for Servicing Windows 7 / 8.1 / 10 Source Images.
- The ToolKitHelper.exe requires Microsoft .NET Framework 4.8.

Known Issues:
=============

- Using ToolKit with Antivirus Programs enabled can affect the ToolKit's operations.
- ToolKit's ToolKitHelper.exe may be flagged as a Virus/Trojan/Malware Program, don't worry it's just a False Positive Sign.
- The ToolKit won't support Post-Servicing of ToolKit serviced source images with other similar tools.
- Windows 7/8.1/10 - Visual C++ Pack is yet to be added.
- Windows 8.1 - Default Metro Apps Pack missing Office OneNote Appx file.
- Windows 8.1 - Integrating Windows Remote Server Administration Tool (RSAT) along with other features will break the Integration with an error code 0x80092004.
- Windows 7/8.1/10 v1507/v1511/v1607/v1703/v1709/v1803 Component removal has been removed temporarily.
- Windows 10 v1809 - Integrating or Installing Windows Updates after the component removal can restore removed components empty resources files/folders.
- Windows 10 v1903/v1909 - Integrating or Installing Windows Updates after the component removal will restore the removed components and this is due to the recent change in Microsoft Update mechanism.
- Windows 10 v1809/v1909 - Removing Internet Explorer breaks DirectX 9.0c Web Installer and Photoshop CC Web Installer.
- Windows 10 v1809/v1909 - It has been reported that Removing Map Control breaks Photos App Image Info.
- Windows 10 v1703/v1709/v1803/v1809/v1903/v1909/v2004 - Custom User Account Picture Integration is not working in Logon Screen although it's been displayed in Start Menu User Icon.
- Windows 10 v1709/v1803/v1809/v1903/v1909/v2004 - It has been reported that in the Format USB Function, the Diskpart command "list" is not working when used within the Script.

General Usage:
==============

- Download the ToolKit archive and ToolKit's Pack files.
- Unblock the downloaded ToolKit archive file by righting clicking on the archive file and choose properties and then click on Unblock button.
- Extract the ToolKit archive to a folder with shorter folder path e.g: C:\ToolKit
- Extract/Copy the Windows Source ISO/DVD Image/Disc contents to ToolKit's <DVD> folder.
- Double Click on Start.cmd and Choose Yes to Run as Administrator.
- Click on ToolKit's Command Window Control Box and Choose Properties.
- If using Windows 7/Windows 8.1 HOST OS then Go To Font Tab and Set the Font to Consolas and Font Size to 16.
- Go to Layout Tab and Increase the Height to 1000 in Screen Buffer Size Group Box.
- Agree to ToolKit's EULA by pressing 'A' Key.
- Press Enter Key to Continue.


Windows 7/ThinPC/Server 2008R2 Usage Order:
===========================================

[A] - Select the Source Images using [Source->Select Source from Source <DVD> Folder] menu.
    
      <Optional> If required to service Source Boot/Recovery images then choose Yes or No when asked.

      Note: Copy the contents of Windows Installation source to ToolKit's <DVD> folder.
      The Toolkit requires a Windows Installation Image to be in a .wim format for servicing.

[B] - <Optional> Integrate the Windows Language Packs using [Integrate->Windows Language Packs] menu.

      Note: You need to download the Windows Language Packs for MSMG ToolKit from the ToolKit's website : https://msmgtoolkit.in
      The Pack contains the Windows Language Pack and WinPE Language Packs files and the Windows Language Packs for MSMG ToolKit
      are uploaded only on request basis due to a very low upload speed here.

      Note: Copy the Windows Language Pack folder to ToolKit's <Packs\LanguagePacks\w7\<Architecture> folder E.g: <Packs\LanguagePacks\w7\x64>.

[C] - <Optional> Integrate the Windows Drivers using [Integrate->Windows Drivers] menu.

      Note: Copy the Driver files/folder to ToolKit's <Drivers\Install\w7\<Architecture> folder E.g: <Drivers\Install\w7\x64>.

[D] - Integrate the required Windows Features (Except Microsoft .NET Framework 3.5) using [Integrate->Windows Features] menu.

      Note: MSMG ToolKit Packs are not included within the ToolKit archive due to its size and instead they are provided separately.
      You need to download the required packs from ToolKit's website https://msmgtoolkit.in and copy them to ToolKit's Packs folder.

	  Supported Packs:
	  
	  <Packs\CustomFiles\w7>				Place Holder for Custom files to be copied to installation image
	  <Packs\Dart\w7>						Microsoft Diagnostics and Recovery Toolset (DaRT) 7.0
	  <Packs\DirectX9c>						Microsoft DirectX 9.0c End-User Runtime
	  <Packs\Games>							Microsoft Windows Classic Games
	  <Packs\IE11>							Microsoft Internet Explorer 11
	  <Packs\LanguagePacks\w7>				Windows Language Packs for installation and WinPE images
	  <Packs\MediaFeaturePack\w7>			Media Feature Pack for N versions of Windows
	  <Packs\NetFX48\w7>					Microsoft .NET Framework 4.8 Runtime
	  <Packs\RDP81>							Remote Desktop Protocol (RDP) 8.1
	  <Packs\RSAT\w7>						Remote Server Administration Tools (RSAT) for Windows
	  <Packs\SystemRestore\w7>				System Restore for Windows Server 2008 R2
	  <Packs\ThinPC>						Windows Thin PC Add-on features pack
	  <Packs\TS\w7>							Terminal Server patch to enable Remote Desktop concurrent connections
	  <Packs\UAP\w7>						Custom User Account Pictures
	  <Packs\UxTheme\w7>					UxTheme patch to enable using custom Themes
	  <Packs\WinRE\w7>						Place Holder for Custom Windows Recovery Environment (Winre.wim) file
	  <Packs\WMF\w7>						Windows Management Framework (WMF) 5.1
  
[E] - Integrate Windows Updates using [Integrate->Windows Updates->Windows Updates] menu.

      Note: The Toolkit supports updates either in .msu/.cab format.
      If using Windows Updates Menu, then Copy the Windows Updates to ToolKit's <Updates\w7\<Architecture> folder E.g: <Updates\w7\x64>.
	  if using WHD Update Pack Menu, then Copy the Windows 7 WHD Update Pack files to ToolKit's <WHD\w7\<Architecture> folder (E.g. <WHD\w7\x64>).

[F] - Removing Windows Component using [Remove->Remove Windows Components using Package List] menu.

	  Note: You need to fill-in the list of components package names in ToolKit's <Bin\Lists\RemovePkgsList.txt> file.
	  The Template for components package names are given in <Bin\Lists\RemovePkgsList_W7_Template.txt> file.

[G] - <Optional> Integrate the required Windows Custom Features using [Integrate->Windows Custom Features] menu.
[H] - <Optional> Customize the Image using [Customize] menu.
[I] - Apply & Save Changes to Source Images using [Apply->Apply & Save Changes to Source Images] menu.
[J] - Re-Build Source Images using [Apply->Re-Build Source Images] menu.


Windows 8.1/Server 2012R2 Usage Order:
======================================

[A] - Select the Source Images using [Source->Select Source from Source <DVD> Folder] menu.
    
      <Optional> If required to service Source Boot/Recovery images then choose Yes or No when asked.

      Note: Copy the contents of Windows Installation source to ToolKit's <DVD> folder.
      The Toolkit requires a Windows Installation Image to be in a .wim format for servicing.

[B] - <Optional> Integrate the Windows Language Packs using [Integrate->Windows Language Packs] menu.

      Note: You need to download the Windows Language Packs for MSMG ToolKit from the ToolKit's website : https://msmgtoolkit.in
      The Pack contains the Windows Language Pack and WinPE Language Packs files and the Windows Language Packs for MSMG ToolKit
      are uploaded only on request basis due to a very low upload speed here.

      Copy the Windows Language Pack folder to <Packs\LanguagePacks\w81\<Architecture> folder E.g: <Packs\LanguagePacks\w81\x64>.

[C] - <Optional> Integrate the Windows Drivers using [Integrate->Windows Drivers] menu.

      Note: Copy the Driver files/folder to ToolKit's <Drivers\Install\w81\<Architecture> folder E.g: <Drivers\Install\w81\x64>.

[D] - Integrate the required Windows Features (Except Microsoft .NET Framework 3.5) using [Integrate->Windows Features] menu.

      Note: MSMG ToolKit Packs are not included within the ToolKit archive due to its size and instead they are provided separately.
      You need to download the required packs from ToolKit's website https://msmgtoolkit.in and copy them to ToolKit's Packs folder.

	  For Microsoft .NET Framework 3.5 Runtime, The Pack folder has been zipped as x86.zip and x64.zip, you need to download and
	  extract them to x86 and x64 folder inside <Packs\NetFX35\w81> folder.

	  Supported Packs:

	  <Packs\Apps\w81>						Default Inbox Metro Apps
	  <Packs\CustomFiles\w81>				Place Holder for Custom files to be copied to installation image
	  <Packs\Dart\w81>						Microsoft Diagnostics and Recovery Toolset (DaRT) 8.1
	  <Packs\Dedup\w81>						Microsoft Data Deduplication Pack
	  <Packs\DirectX9c>						Microsoft DirectX 9.0c End-User Runtime
	  <Packs\Games>							Microsoft Windows Classic Games
	  <Packs\LanguagePacks\w81>				Windows Language Packs for installation and WinPE images
	  <Packs\MediaFeaturePack\w81>			Media Feature Pack for N versions of Windows
	  <Packs\NetFX35\w81>					Microsoft .NET Framework 3.5 Runtime
	  <Packs\NetFX48\w81>					Microsoft .NET Framework 4.8 Runtime
	  <Packs\PreActTokens\w81>				Place Holder for Pre-Actiavtation Data Tokens
	  <Packs\RSAT\w81>						Remote Server Administration Tools (RSAT) for Windows
	  <Packs\Sidebar\w81>					Windows Sidebar Gadget
	  <Packs\TS\w81>						Terminal Server patch to enable Remote Desktop concurrent connections
	  <Packs\UAP\w81>						Custom User Account Pictures
	  <Packs\UxTheme\w81>					UxTheme patch to enable using custom Themes
	  <Packs\WinRE\w81>						Place Holder for Custom Windows Recovery Environment (Winre.wim) file
	  <Packs\WinToGo\w81>					Windows Portable Workspace Creator (Windows To Go)
	  <Packs\WMF\w81>						Windows Management Framework (WMF) 5.1
      
[E] - Integrate Windows Updates using [Integrate->Windows Updates->Windows Updates] menu.

      Note: The Toolkit supports updates either in .msu/.cab format.
      If using Windows Updates Menu, then Copy the Windows Updates to ToolKit's <Updates\w81\<Architecture> folder E.g: <Updates\w81\x64>.
	  if using WHD Update Pack Menu, then Copy the Windows 8.1 WHD Update Pack files to ToolKit's <WHD\w81\<Architecture> folder (E.g. <WHD\w81\x64>).

[F] - <Optional> Integrate Windows Setup Media Updates using [Integrate->Windows Updates->Windows Setup Media Updates] menu.

	  Note: Only if WHD Update Pack is Integrated to Windows Installation Boot Image.
	  
[G] - Removing Windows Component using [Remove->Remove Windows Components using Package List] menu.

	  Note: You need to fill-in the list of components package names in ToolKit's <Bin\Lists\RemovePkgsList.txt> file.
	  The Template for components package names are given in <Bin\Lists\RemovePkgsList_W81_Template.txt> file.

[H] - <Optional> Integrate the required Windows Custom Features using [Integrate->Windows Custom Features] menu.
[I] - <Optional> Customize the Image using [Customize] menu.
[J] - Cleanup the Source Image using [Apply->Cleanup Source Images] menu.
[K] - Integrate Microsoft .NET Framework 3.5 Feature using [Integrate->Windows Features->Microsoft .NET Framework 3.5) menu.
[L] - Apply & Save Changes to Source Images using [Apply->Apply & Save Changes to Source Images] menu.
[M] - Re-Build Source Images using [Apply->Re-Build Source Images] menu.


Windows 10 v1507/v1511/v1607/v1703/v1709/V1803 Client/Server Usage Order:
=========================================================================

[A] - Select the Source Images using [Source->Select Source from Source <DVD> Folder] menu.
    
      <Optional> If required to service Source Boot/Recovery images then choose Yes or No when asked.

      Note: Copy the contents of Windows Installation source to ToolKit's <DVD> folder.
      The Toolkit requires a Windows Installation Image to be in a .wim format for servicing.

[B] - <Optional> Integrate the Windows Language Packs using [Integrate->Windows Language Packs] menu.

      Note: You need to download the Windows Language Packs for MSMG ToolKit from the ToolKit's website : https://msmgtoolkit.in
      The Pack contains the Windows Language Pack and WinPE Language Packs files and the Windows Language Packs for MSMG ToolKit
      are uploaded only on request basis due to a very low upload speed here.

      Copy the Windows Language Pack folder to <Packs\LanguagePacks\w10\<Architecture> folder E.g: <Packs\LanguagePacks\w10\x64>.

[C] - <Optional> Integrate the Windows Drivers using [Integrate->Windows Drivers] menu.

      Note: Copy the Driver files/folder to ToolKit's <Drivers\Install\w10\<Architecture> folder E.g: <Drivers\Install\w10\x64>.

[D] - Integrate the required Windows Features (Except Microsoft .NET Framework 3.5) using [Integrate->Windows Features] menu.

      Note: MSMG ToolKit Packs are not included within the ToolKit archive due to its size and instead they are provided separately.
      You need to download the required packs from ToolKit's website https://msmgtoolkit.in and copy them to ToolKit's Packs folder.

	  Supported Packs:

	  <Packs\Apps\w10\<OSVersion>							Default Inbox Metro Apps
	  <Packs\Braille\<OSVersion>							Windows Accessibility Braille
	  <Packs\CustomFiles\w10>								Place Holder for Custom files to be copied to installation image
	  <Packs\Dart\w10>										Microsoft Diagnostics and Recovery Toolset (DaRT) 10
	  <Packs\Dedup\w10\<OSVersion>							Microsoft Data Deduplication Pack
	  <Packs\DirectX9c>										Microsoft DirectX 9.0c End-User Runtime
	  <Packs\EdgeBrowser\<OSVersion>						Microsoft Edge Browser App for LTSB/LTSC and Server versions of Windows
	  <Packs\EdgeChromium>									Microsoft Edge Chromium Browser
	  <Packs\Games>											Microsoft Windows Classic Games
	  <Packs\LanguagePacks\w10\<OSVersion>					Windows Language Packs for installation and WinPE images
	  <Packs\MediaFeaturePack\w10\<OSVersion>				Media Feature Pack for N versions of Windows
	  <Packs\MultimediaRestrictedCodecs\w10\<OSVersion>		Multimedia Restricted Codecs for N and Server versions of Windows
	  <Packs\NetFX35\w10\<OSVersion>						Microsoft .NET Framework 3.5 Runtime
	  <Packs\NetFX48\w10>									Microsoft .NET Framework 4.8 Runtime for Windows 10 v1607, v1703, v1709, v1803 and v1809
	  <Packs\NetFX462>										Microsoft .NET Framework 4.6.2 Runtime for Windows 10 v1507 and v1511
	  <Packs\OfficeUWP>										Microsoft Office Desktop UWP Apps
	  <Packs\OpenSSH\<OSVersion>							Open Secure Shell (SSH) Client and Server
	  <Packs\PortableDevices>								Windows Mobile Portable Devices
	  <Packs\RSAT\w10\10.0.14393>							Remote Server Administration Tools (RSAT) for Windows 10 v1607 and v1703
	  <Packs\RSAT\w10\10.0.16299>							Remote Server Administration Tools (RSAT) for Windows 10 v1709
	  <Packs\RSAT\w10\10.0.17134>							Remote Server Administration Tools (RSAT) for Windows 10 v1803
	  <Packs\Sidebar\w10>									Windows Sidebar Gadget
	  <Packs\Skins>											Custom Skins for Windows Calculator, Media Player and Photo Viewer
	  <Packs\SystemRestore\w10\<OSVersion>					System Restore for Server versions of Windows
	  <Packs\TS\w10>										Terminal Server patch to enable Remote Desktop concurrent connections
	  <Packs\UAP\w10>										Custom User Account Pictures
	  <Packs\UxTheme\w10>									UxTheme patch to enable Custom Themes support
	  <Packs\Win32Calc>										Windows Classic Calculator for LTSB/LTSC and Server versions of Windows
	  <Packs\WinRE\w10>										Place Holder for Custom Windows Recovery Environment (Winre.wim) file
	  <Packs\WinToGo\w10\<OSVersion>						Windows Portable Workspace Creator (Windows To Go)
	  <Packs\WSL\<OSVersion>								Windows Subsystems for Linux (WSL) for Server versions of Windows

[E] - Integrate Windows Updates using [Integrate->Windows Updates->Windows Updates] menu.

      Note: The Toolkit supports updates either in .msu/.cab format.
      If using Windows Updates Menu, then Copy the Windows Updates to ToolKit's <Updates\w10\<Architecture> folder E.g: <Updates\w10\x64>.
	  if using WHD Update Pack Menu, then Copy the Windows 10 WHD Update Pack files to ToolKit's <WHD\w10\<Architecture> folder (E.g. <WHD\w10\x64>).

      Copy Windows Cumulative Update file to <WHD\w10\<Architecture>\Cumulative> folder (E.g. <WHD\w10\x64\Cumulative>).
      Copy Windows Dynamic Update files to <WHD\w10\<Architecture>\Dynamic> folder (E.g. <WHD\w10\x64\Dynamic>).
      Copy Windows Flash Player Update file to <WHD\w10\<Architecture>\FlashPlayer> folder (E.g. <WHD\w10\x64\FlashPlayer>).
      Copy Windows .Net Cumulative Update file to <WHD\w10\<Architecture>\NetCumulative> folder (E.g. <WHD\w10\x64\NetCumulative>).
      Copy Windows Servicing Stack Update file to <WHD\w10\<Architecture>\ServicingStack> folder (E.g. <WHD\w10\x64\ServicingStack>).
      Copy Windows Setup Media Update files to <WHD\w10\<Architecture>\SetupMedia> folder (E.g. <WHD\w10\x64\SetupMedia>).
      Copy Windows WinPE Update files to <WHD\w10\<Architecture>\WinPE> folder (E.g. <WHD\w10\x64\WinPE>).

[F] - Remove all required Windows Components using [Remove->Remove Windows Components] menu.

[G] - <Optional> Integrate Windows Setup Media Updates using [Integrate->Windows Updates->Windows Setup Media Updates] menu.

	  Note: Only if WHD Update Pack is Integrated to Windows Installation Boot Image.

[H] - <Optional> Integrate the required Windows Custom Features using [Integrate->Windows Custom Features] menu.
[I] - <Optional> Customize the Image using [Customize] menu.
[J] - Cleanup the Source Image using [Apply->Cleanup Source Images] menu.
[K] - Integrate Microsoft .NET Framework 3.5 Feature using [Integrate->Windows Features->Microsoft .NET Framework 3.5) menu.
[L] - Apply & Save Changes to Source Images using [Apply->Apply & Save Changes to Source Images] menu.
[M] - Re-Build Source Images using [Apply->Re-Build Source Images] menu.


Windows 10 v1809 Client/Server Usage Order:
===========================================

[A] - Select the Source Images using [Source->Select Source from Source <DVD> Folder] menu.
    
      <Optional> If required to service Source Boot/Recovery images then choose Yes or No when asked.

      Note: Copy the contents of Windows Installation source to ToolKit's <DVD> folder.
      The Toolkit requires a Windows Installation Image to be in a .wim format for servicing.

[B] - <Optional> Integrate the Windows Language Packs using [Integrate->Windows Language Packs] menu.

      Note: You need to download the Windows Language Packs for MSMG ToolKit from the ToolKit's website : https://msmgtoolkit.in
      The Pack contains the Windows Language Pack and WinPE Language Packs files and the Windows Language Packs for MSMG ToolKit
      are uploaded only on request basis due to a very low upload speed here.

      Copy the Windows Language Pack folder to <Packs\LanguagePacks\w10\<Architecture> folder E.g: <Packs\LanguagePacks\w10\x64>.

[C] - <Optional> Integrate the Windows Drivers using [Integrate->Windows Drivers] menu.

      Note: Copy the Driver files/folder to ToolKit's <Drivers\Install\w10\<Architecture> folder E.g: <Drivers\Install\w10\x64>.

[D] - Integrate the required Windows Features (Except Microsoft .NET Framework 3.5) using [Integrate->Windows Features] menu.

      Note: MSMG ToolKit Packs are not included within the ToolKit archive due to its size and instead they are provided separately.
      You need to download the required packs from ToolKit's website https://msmgtoolkit.in and copy them to ToolKit's Packs folder.

	  Supported Packs:

	  <Packs\Apps\w10\<OSVersion>							Default Inbox Metro Apps
	  <Packs\Braille\<OSVersion>							Windows Accessibility Braille
	  <Packs\CustomFiles\w10>								Place Holder for Custom files to be copied to installation image
	  <Packs\Dart\w10>										Microsoft Diagnostics and Recovery Toolset (DaRT) 10
	  <Packs\Dedup\w10\<OSVersion>							Microsoft Data Deduplication Pack
	  <Packs\DirectX9c>										Microsoft DirectX 9.0c End-User Runtime
	  <Packs\EdgeBrowser\<OSVersion>						Microsoft Edge Browser App for LTSC and Server versions of Windows
	  <Packs\EdgeChromium>									Microsoft Edge Chromium Browser
	  <Packs\Games>											Microsoft Windows Classic Games
	  <Packs\LanguagePacks\w10\<OSVersion>					Windows Language Packs for installation and WinPE images
	  <Packs\MediaFeaturePack\w10\<OSVersion>				Media Feature Pack for N versions of Windows
	  <Packs\MultimediaRestrictedCodecs\w10\<OSVersion>		Multimedia Restricted Codecs for N and Server versions of Windows
	  <Packs\NetFX35\w10\<OSVersion>						Microsoft .NET Framework 3.5 Runtime
	  <Packs\NetFX48\w10>									Microsoft .NET Framework 4.8 Runtime for Windows 10 v1607, v1703, v1709, v1803 and v1809
	  <Packs\OfficeUWP>										Microsoft Office Desktop UWP Apps
	  <Packs\OpenSSH\<OSVersion>							Open Secure Shell (SSH) Client and Server
	  <Packs\PortableDevices>								Windows Mobile Portable Devices
	  <Packs\Sidebar\w10>									Windows Sidebar Gadget
	  <Packs\Skins>											Custom Skins for Windows Calculator, Media Player and Photo Viewer
	  <Packs\TS\w10>										Terminal Server patch to enable Remote Desktop concurrent connections
	  <Packs\UAP\w10>										Custom User Account Pictures
	  <Packs\UxTheme\w10>									UxTheme patch to enable Custom Themes support
	  <Packs\Win32Calc>										Windows Classic Calculator for LTSB/LTSC and Server versions of Windows
	  <Packs\WinRE\w10>										Place Holder for Custom Windows Recovery Environment (Winre.wim) file
	  <Packs\WinToGo\w10\<OSVersion>						Windows Portable Workspace Creator (Windows To Go)
	  <Packs\WSL\<OSVersion>								Windows Subsystems for Linux (WSL) for Server versions of Windows

[E] - <Optional> Cleanup the Source Image using [Apply->Cleanup Source Images] menu.

	  Note: Only if using Step [F]

[F] - Remove all required Windows Components using [Remove->Remove Windows Components] menu.

	  Note: Only for Client Editions

[G] - Integrate Windows Updates using [Integrate->Windows Updates->Windows Updates] menu.

      Note: The Toolkit supports updates either in .msu/.cab format.
      If using Windows Updates Menu, then Copy the Windows Updates to ToolKit's <Updates\w10\<Architecture> folder E.g: <Updates\w10\x64>.
	  if using WHD Update Pack Menu, then Copy the Windows 10 WHD Update Pack files to ToolKit's <WHD\w10\<Architecture> folder (E.g. <WHD\w10\x64>).

      Copy Windows Cumulative Update file to <WHD\w10\<Architecture>\Cumulative> folder (E.g. <WHD\w10\x64\Cumulative>).
      Copy Windows Dynamic Update files to <WHD\w10\<Architecture>\Dynamic> folder (E.g. <WHD\w10\x64\Dynamic>).
      Copy Windows Flash Player Update file to <WHD\w10\<Architecture>\FlashPlayer> folder (E.g. <WHD\w10\x64\FlashPlayer>).
      Copy Windows .Net Cumulative Update file to <WHD\w10\<Architecture>\NetCumulative> folder (E.g. <WHD\w10\x64\NetCumulative>).
      Copy Windows Servicing Stack Update file to <WHD\w10\<Architecture>\ServicingStack> folder (E.g. <WHD\w10\x64\ServicingStack>).
      Copy Windows Setup Media Update files to <WHD\w10\<Architecture>\SetupMedia> folder (E.g. <WHD\w10\x64\SetupMedia>).
      Copy Windows WinPE Update files to <WHD\w10\<Architecture>\WinPE> folder (E.g. <WHD\w10\x64\WinPE>).

[H] - <Optional> Integrate Windows Setup Media Updates using [Integrate->Windows Updates->Windows Setup Media Updates] menu.

	  Note: Only if WHD Update Pack is Integrated to Windows Installation Boot Image.
	  
[I] - <Optional> Integrate the required Windows Custom Features using [Integrate->Windows Custom Features] menu.
[J] - <Optional> Customize the Image using [Customize] menu.
[K] - Cleanup the Source Image using [Apply->Cleanup Source Images] menu.
[L] - Integrate Microsoft .NET Framework 3.5 Feature using [Integrate->Windows Features->Microsoft .NET Framework 3.5) menu.
[M] - Apply & Save Changes to Source Images using [Apply->Apply & Save Changes to Source Images] menu.
[N] - Re-Build Source Images using [Apply->Re-Build Source Images] menu.


Windows 10 v1903/v1909 Client/Server Usage Order:
=================================================

[A] - Select the Source Images using [Source->Select Source from Source <DVD> Folder] menu.
    
      <Optional> If required to service Source Boot/Recovery images then choose Yes or No when asked.

      Note: Copy the contents of Windows Installation source to ToolKit's <DVD> folder.
      The Toolkit requires a Windows Installation Image to be in a .wim format for servicing.

[B] - <Optional> Integrate the Windows Language Packs using [Integrate->Windows Language Packs] menu.

      Note: You need to download the Windows Language Packs for MSMG ToolKit from the ToolKit's website : https://msmgtoolkit.in
      The Pack contains the Windows Language Pack and WinPE Language Packs files and the Windows Language Packs for MSMG ToolKit
      are uploaded only on request basis due to a very low upload speed here.

      Copy the Windows Language Pack folder to <Packs\LanguagePacks\w10\<Architecture> folder E.g: <Packs\LanguagePacks\w10\x64>.

[C] - <Optional> Integrate the Windows Drivers using [Integrate->Windows Drivers] menu.

      Note: Copy the Driver files/folder to ToolKit's <Drivers\Install\w10\<Architecture> folder E.g: <Drivers\Install\w10\x64>.

[D] - Integrate the required Windows Features (Except Microsoft .NET Framework 3.5) using [Integrate->Windows Features] menu.

      Note: MSMG ToolKit Packs are not included within the ToolKit archive due to its size and instead they are provided separately.
      You need to download the required packs from ToolKit's website https://msmgtoolkit.in and copy them to ToolKit's Packs folder.

	  Supported Packs:

	  <Packs\Apps\w10\<OSVersion>							Default Inbox Metro Apps
	  <Packs\Braille\<OSVersion>							Windows Accessibility Braille
	  <Packs\CustomFiles\w10>								Place Holder for Custom files to be copied to installation image
	  <Packs\Dart\w10>										Microsoft Diagnostics and Recovery Toolset (DaRT) 10
	  <Packs\Dedup\w10\<OSVersion>							Microsoft Data Deduplication Pack
	  <Packs\DirectX9c>										Microsoft DirectX 9.0c End-User Runtime
	  <Packs\EdgeBrowser\<OSVersion>						Microsoft Edge Browser App for LTSC and Server versions of Windows
	  <Packs\EdgeChromium>									Microsoft Edge Chromium Browser
	  <Packs\Games>											Microsoft Windows Classic Games
	  <Packs\LanguagePacks\w10\<OSVersion>					Windows Language Packs for installation and WinPE images
	  <Packs\MediaFeaturePack\w10\<OSVersion>				Media Feature Pack for N versions of Windows
	  <Packs\MultimediaRestrictedCodecs\w10\<OSVersion>		Multimedia Restricted Codecs for N and Server versions of Windows
	  <Packs\NetFX35\w10\<OSVersion>						Microsoft .NET Framework 3.5 Runtime
	  <Packs\OfficeUWP>										Microsoft Office Desktop UWP Apps
	  <Packs\OpenSSH\<OSVersion>							Open Secure Shell (SSH) Client and Server
	  <Packs\PortableDevices>								Windows Mobile Portable Devices
	  <Packs\Sidebar\w10>									Windows Sidebar Gadget
	  <Packs\Skins>											Custom Skins for Windows Calculator, Media Player and Photo Viewer
	  <Packs\TS\w10>										Terminal Server patch to enable Remote Desktop concurrent connections
	  <Packs\UAP\w10>										Custom User Account Pictures
	  <Packs\UxTheme\w10>									UxTheme patch to enable Custom Themes support
	  <Packs\Win32Calc>										Windows Classic Calculator for LTSB/LTSC and Server versions of Windows
	  <Packs\WinRE\w10>										Place Holder for Custom Windows Recovery Environment (Winre.wim) file
	  <Packs\WinToGo\w10\<OSVersion>						Windows Portable Workspace Creator (Windows To Go)
	  <Packs\WSL\<OSVersion>								Windows Subsystems for Linux (WSL) for Server versions of Windows

[E] - Integrate Windows Updates using [Integrate->Windows Updates->Windows Updates] menu.

      Note: The Toolkit supports updates either in .msu/.cab format.
      If using Windows Updates Menu, then Copy the Windows Updates to ToolKit's <Updates\w10\<Architecture> folder E.g: <Updates\w10\x64>.
	  if using WHD Update Pack Menu, then Copy the Windows 10 WHD Update Pack files to ToolKit's <WHD\w10\<Architecture> folder (E.g. <WHD\w10\x64>).

      Copy Windows Cumulative Update file to <WHD\w10\<Architecture>\Cumulative> folder (E.g. <WHD\w10\x64\Cumulative>).
      Copy Windows Dynamic Update files to <WHD\w10\<Architecture>\Dynamic> folder (E.g. <WHD\w10\x64\Dynamic>).
      Copy Windows Enablement Update files to <WHD\w10\<Architecture>\Enablement> folder (E.g. <WHD\w10\x64\Enablement>).
      Copy Windows Flash Player Update file to <WHD\w10\<Architecture>\FlashPlayer> folder (E.g. <WHD\w10\x64\FlashPlayer>).
      Copy Windows .Net Cumulative Update file to <WHD\w10\<Architecture>\NetCumulative> folder (E.g. <WHD\w10\x64\NetCumulative>).
      Copy Windows Servicing Stack Update file to <WHD\w10\<Architecture>\ServicingStack> folder (E.g. <WHD\w10\x64\ServicingStack>).
      Copy Windows Setup Media Update files to <WHD\w10\<Architecture>\SetupMedia> folder (E.g. <WHD\w10\x64\SetupMedia>).
      Copy Windows WinPE Update files to <WHD\w10\<Architecture>\WinPE> folder (E.g. <WHD\w10\x64\WinPE>).

[F] - <Optional> Integrate Windows Setup Media Updates using [Integrate->Windows Updates->Windows Setup Media Updates] menu.

	  Note: Only if WHD Update Pack is Integrated to Windows Installation Boot Image.

[G] - Remove all required Windows Components using [Remove->Remove Windows Components] menu.

	  Note: Only for Client Editions.

[H] - <Optional> Integrate the required Windows Custom Features using [Integrate->Windows Custom Features] menu.
[I] - <Optional> Customize the Image using [Customize] menu.
[J] - Cleanup the Source Image using [Apply->Cleanup Source Images] menu.
[K] - Integrate Microsoft .NET Framework 3.5 Feature using [Integrate->Windows Features->Microsoft .NET Framework 3.5) menu.
[L] - Apply & Save Changes to Source Images using [Apply->Apply & Save Changes to Source Images] menu.
[M] - Re-Build Source Images using [Apply->Re-Build Source Images] menu.


Windows 10 v2004 Client/Server Usage Order:
===========================================

[A] - Select the Source Images using [Source->Select Source from Source <DVD> Folder] menu.
    
      <Optional> If required to service Source Boot/Recovery images then choose Yes or No when asked.

      Note: Copy the contents of Windows Installation source to ToolKit's <DVD> folder.
      The Toolkit requires a Windows Installation Image to be in a .wim format for servicing.

[B] - <Optional> Integrate the Windows Language Packs using [Integrate->Windows Language Packs] menu.

      Note: You need to download the Windows Language Packs for MSMG ToolKit from the ToolKit's website : https://msmgtoolkit.in
      The Pack contains the Windows Language Pack and WinPE Language Packs files and the Windows Language Packs for MSMG ToolKit
      are uploaded only on request basis due to a very low upload speed here.

      Copy the Windows Language Pack folder to <Packs\LanguagePacks\w10\<Architecture> folder E.g: <Packs\LanguagePacks\w10\x64>.

[C] - <Optional> Integrate the Windows Drivers using [Integrate->Windows Drivers] menu.

      Note: Copy the Driver files/folder to ToolKit's <Drivers\Install\w10\<Architecture> folder E.g: <Drivers\Install\w10\x64>.

[D] - Integrate the required Windows Features (Except Microsoft .NET Framework 3.5) using [Integrate->Windows Features] menu.

      Note: MSMG ToolKit Packs are not included within the ToolKit archive due to its size and instead they are provided separately.
      You need to download the required packs from ToolKit's website https://msmgtoolkit.in and copy them to ToolKit's Packs folder.

	  Supported Packs:

	  <Packs\Apps\w10\<OSVersion>							Default Inbox Metro Apps
	  <Packs\Braille\<OSVersion>							Windows Accessibility Braille
	  <Packs\CustomFiles\w10>								Place Holder for Custom files to be copied to installation image
	  <Packs\Dart\w10>										Microsoft Diagnostics and Recovery Toolset (DaRT) 10
	  <Packs\Dedup\w10\<OSVersion>							Microsoft Data Deduplication Pack
	  <Packs\DirectX9c>										Microsoft DirectX 9.0c End-User Runtime
	  <Packs\EdgeBrowser\<OSVersion>						Microsoft Edge Browser App for LTSC and Server versions of Windows
	  <Packs\EdgeChromium>									Microsoft Edge Chromium Browser
	  <Packs\Games>											Microsoft Windows Classic Games
	  <Packs\LanguagePacks\w10\<OSVersion>					Windows Language Packs for installation and WinPE images
	  <Packs\MediaFeaturePack\w10\<OSVersion>				Media Feature Pack for N versions of Windows
	  <Packs\MultimediaRestrictedCodecs\w10\<OSVersion>		Multimedia Restricted Codecs for N and Server versions of Windows
	  <Packs\NetFX35\w10\<OSVersion>						Microsoft .NET Framework 3.5 Runtime
	  <Packs\OfficeUWP>										Microsoft Office Desktop UWP Apps
	  <Packs\OpenSSH\<OSVersion>							Open Secure Shell (SSH) Client and Server
	  <Packs\PortableDevices>								Windows Mobile Portable Devices
	  <Packs\Sidebar\w10>									Windows Sidebar Gadget
	  <Packs\Skins>											Custom Skins for Windows Calculator, Media Player and Photo Viewer
	  <Packs\TS\w10>										Terminal Server patch to enable Remote Desktop concurrent connections
	  <Packs\UAP\w10>										Custom User Account Pictures
	  <Packs\UxTheme\w10>									UxTheme patch to enable Custom Themes support
	  <Packs\Win32Calc>										Windows Classic Calculator for LTSB/LTSC and Server versions of Windows
	  <Packs\WinRE\w10>										Place Holder for Custom Windows Recovery Environment (Winre.wim) file
	  <Packs\WSL\<OSVersion>								Windows Subsystems for Linux (WSL) for Server versions of Windows

[E] - Integrate Windows Updates using [Integrate->Windows Updates->Windows Updates] menu.

      Note: The Toolkit supports updates either in .msu/.cab format.
      If using Windows Updates Menu, then Copy the Windows Updates to ToolKit's <Updates\w10\<Architecture> folder E.g: <Updates\w10\x64>.
	  if using WHD Update Pack Menu, then Copy the Windows 10 WHD Update Pack files to ToolKit's <WHD\w10\<Architecture> folder (E.g. <WHD\w10\x64>).

      Copy Windows Cumulative Update file to <WHD\w10\<Architecture>\Cumulative> folder (E.g. <WHD\w10\x64\Cumulative>).
      Copy Windows Dynamic Update files to <WHD\w10\<Architecture>\Dynamic> folder (E.g. <WHD\w10\x64\Dynamic>).
      Copy Windows Flash Player Update file to <WHD\w10\<Architecture>\FlashPlayer> folder (E.g. <WHD\w10\x64\FlashPlayer>).
      Copy Windows .Net Cumulative Update file to <WHD\w10\<Architecture>\NetCumulative> folder (E.g. <WHD\w10\x64\NetCumulative>).
      Copy Windows Servicing Stack Update file to <WHD\w10\<Architecture>\ServicingStack> folder (E.g. <WHD\w10\x64\ServicingStack>).
      Copy Windows Setup Media Update files to <WHD\w10\<Architecture>\SetupMedia> folder (E.g. <WHD\w10\x64\SetupMedia>).
      Copy Windows WinPE Update files to <WHD\w10\<Architecture>\WinPE> folder (E.g. <WHD\w10\x64\WinPE>).

[F] - <Optional> Integrate Windows Setup Media Updates using [Integrate->Windows Updates->Windows Setup Media Updates] menu.

	  Note: Only if WHD Update Pack is Integrated to Windows Installation Boot Image.

[G] - Remove all required Windows Components using [Remove->Remove Windows Components] menu.

	  Note: Only for Client Editions.

[H] - <Optional> Integrate the required Windows Custom Features using [Integrate->Windows Custom Features] menu.
[I] - <Optional> Customize the Image using [Customize] menu.
[J] - Cleanup the Source Image using [Apply->Cleanup Source Images] menu.
[K] - Integrate Microsoft .NET Framework 3.5 Feature using [Integrate->Windows Features->Microsoft .NET Framework 3.5) menu.
[L] - Apply & Save Changes to Source Images using [Apply->Apply & Save Changes to Source Images] menu.
[M] - Re-Build Source Images using [Apply->Re-Build Source Images] menu.
