# WSL Subsystem Development Environment Setup

## System Requirements

| System Requirements                                          | Download Link                                                |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Windows 10 version 2004 and later (build 19041 and later) or Windows 11 |                                                              |
| For x64 systems: Linux kernel update package                 | [wsl_update_x64.msi](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi  ) |

## WSL Subsystem Download and Import

- To enable the Windows Subsystem for Linux, you must first enable the optional "Windows Subsystem for Linux" feature before you can install a Linux distribution on Windows.

  Open PowerShell **as Administrator** (Start menu > "PowerShell" > right-click > "Run as administrator"), and then enter the following command:

  ```
  dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
  ```

  ![image-20250310184537535](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250310184537535.png)

- This is available for Windows 10 version 2004 and later (build 19041 and later) or Windows 11. To check the Windows version and build number, press the Windows logo key + R, type "winver", and select "OK".

  ![image-20250310185106744](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250310185106744.png)

- Enable the Virtual Machine feature. Before installing WSL 2, you must enable the "Virtual Machine Platform" optional feature. The computer requires [virtualization feature](https://learn.microsoft.com/zh-cn/windows/wsl/troubleshooting#error-0x80370102-the-virtual-machine-could-not-be-started-because-a-required-feature-is-not-installed) to use this feature.

  Open PowerShell **as Administrator** and run:

  ```
  dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
  ```

  ![image-20250310190106392](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250310190106392.png)

- You need to install the Linux kernel update package in order to run WSL in the Windows OS image.

  | System Architecture | Download Link                                                |
  | -------- | ------------------------------------------------------------ |
  | x64      | [wsl_update_x64.msi](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) |

- Restart the computer. Be sure to restart, otherwise errors will occur later.

- Download the fbb_ws63_wsl distribution package. Download link: https://hispark-obs.obs.cn-east-3.myhuaweicloud.com/fbb_ws63_wsl.tar

  ![image-20250311161220485](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250311161220485.png)

- After the download completes, place the archive on the desktop or in another directory. The desktop is used as an example here (path: C:/Users/Administrator/Desktop/fbb_ws63_wsl.tar). At the same time, create a new folder on a non-system drive. Here, an ubuntu folder is created on drive F (path: F:/ubuntu/).

  Open PowerShell **as Administrator** and run:

  ```
  wsl --import fbb_ws63 F:/ubuntu/ C:/Users/Administrator/Desktop/fbb_ws63_wsl.tar
  ```

- After running, wait for the import to complete. Upon success, the following files will be under the F:/ubuntu/ directory.

  ![image-20250310191219674](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250310191219674.png)

  ![image-20250310191203544](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250310191203544.png)

- Restart the computer. Be sure to restart, otherwise the system will be very laggy later.

- After the restart, check whether the WSL subsystem was installed successfully.

  Open PowerShell and run:

  ```
  wsl --list
  ```

  ![image-20250310194511923](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250310194511923.png)

- Install [vscode](https://vscode.download.prss.microsoft.com/dbazure/download/stable/6609ac3d66f4eade5cf376d1cb76f13985724bcb/VSCodeUserSetup-x64-1.98.0.exe). The installation steps are not described here; just follow the custom installation. A successful installation is shown below. Download link: https://vscode.download.prss.microsoft.com/dbazure/download/stable/6609ac3d66f4eade5cf376d1cb76f13985724bcb/VSCodeUserSetup-x64-1.98.0.exe

  ![image-20250310194000292](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250310194000292.png)

- Open VSCode, search for "remote" in the Extensions, and select "Remote Development". Wait for the download to complete.

  ![image-20250310194404035](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250310194404035.png)

- If you need Chinese display, search for "chinese" in the Extensions, select "chinese (Simplified)", and wait for the installation to complete. A "Change Language and Restart" message will pop up in the bottom right corner; click to confirm.

![image-20250310194930378](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250310194930378.png)

![image-20250310195122151](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250310195122151.png)

- In VSCode, select "Remote Explorer", choose "fbb_ws63", and select "Connect in Current Window".

  ![image-20250310200852622](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250310200852622.png)

- Create a new "Terminal" in the VSCode interface.

  ![image-20250310203406547](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250310203406547.png)

- Below the "Terminal" in the VSCode interface, a terminal window will pop up.
  
  ![image-20250311113220441](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250311113220441.png)
  
  
