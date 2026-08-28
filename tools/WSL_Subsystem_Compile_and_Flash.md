# NearLink Code Compilation

## NearLink Code Download

- Open VSCode, and open the "fbb_ws63" subsystem in the "Remote Explorer".

  ![image-20250311110526878](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250311110526878.png)

- Create a new terminal in the "Terminal".

  ![image-20250311110825993](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250311110825993.png)


- In the new terminal, enter the command `git clone https://gitee.com/HiSpark/fbb_ws63.git` to download the code. Wait for the download to complete.

![image-20240807151920249](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20240807151920249.png)

## Import NearLink Code into VSCode

- After the download completes, select "Open Folder" in the "Explorer".

  ![image-20250311111016027](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250311111016027.png)

- In the dialog box, select the "/root/fbb_ws63/src" directory and click OK.

  ![image-20250311111103585](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250311111103585.png)

## NearLink Code Compilation

- Execute the command in the terminal command line:

  ```
  cd fbb_ws63/src
  ```

- Execute the corresponding command in the src directory to perform the corresponding operation. The parameters and descriptions are as follows:

  | Parameter  | Example                                              | Description                                                |
  | ---------- | ---------------------------------------------- | ---------------------------------------------------- |
  | None       | python3 build.py ws63-liteos-app               | Starts incremental compilation of the ws63-liteos-app target. |
  | -c         | python3 build.py -c ws63-liteos-app            | Starts full compilation of the ws63-liteos-app target. |
  | menuconfig | python3 build.py -c ws63-liteos-app menuconfig | Starts the menuconfig graphical configuration interface for the ws63-liteos-app target. |

- Menuconfig configuration: Run the "python3 build.py -c ws63-liteos-app menuconfig" script to start the Menuconfig program. Users can configure compilation and system functions through Menuconfig.

  ![image-20250311114126273](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250311114126273.png)

- The Menuconfig operations are described in the table below. Shortcut keys can be entered in the Menuconfig interface for configuration.

  | Shortcut Key | Description                 |
  | ---------- | ------------------------ |
  | Space, Enter | Select or deselect.      |
  | ESC        | Return to the parent menu, or exit the interface. |
  | Q          | Exit the interface.      |
  | S          | Save the configuration.  |
  | F          | Display the help menu.   |

- Here, "Enable Sample > Enable the Sample of peripheral > Support BLINKY SAMPLE" is used as an example.

  ![image-20250311114606721](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250311114606721.png)
  
- Press "Enter" to select each item in sequence, then press "ESC" to exit. In the dialog box that appears, press "y" to select yes.

  ![image-20250311115322015](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250311115322015.png)

- Enter "python3 build.py ws63-liteos-app" in the terminal.

  ```
  python3 build.py ws63-liteos-app
  ```
  
- Wait for the compilation to complete. A successful compilation is shown below.
  
  ![image-20250311115606569](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250311115606569.png)


## Image Flashing


- Hardware setup: Use a Type-C cable to connect the board to the PC.

  ![image-20240801173105245](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20240801173105245.png)

- Install the driver "CH341SER Driver" ([CH341SER Driver download address](https://www.wch.cn/downloads/CH341SER_EXE.html). **If the link is invalid or cannot be downloaded, please download it yourself via Baidu**). Before installing the CH341SER driver, the board must be connected to the PC. Click Install. **"Driver installed successfully" indicates success; if "Driver pre-installation successful" appears, it means the installation failed**.

    ![image-20240801173439645](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20240801173439645.png)

    ![image-20240801173618611](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20240801173618611.png)

- Download the BurnTool flashing tool and extract it.

    ```hljs
    Link: https://gitee.com/hihope_iot/near-link/tree/master/tools
    ```

- Open the flashing tool, select the corresponding serial port. Open the flashing tool, click the "Option" option, select the corresponding target. WS63E and WS63 belong to the same series; select WS63.

  

  ![image.png](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/21.png)

  

- Select the flashing file. Example path is (select ws63-liteos-app-all.fwpkg):

  ```hljs
  F:\ubuntu\rootfs\root\fbb_ws63\src\output\ws63\fwpkg\ws63-liteos-app
  ```
  
- Check the "Auto Burn" and "Auto disconnect" options, click connect to connect, then press the RST button on the development board to start flashing.

- The result after flashing is complete is as follows:

  
  ![image.png](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/22.png)

  (4) Open the serial port tool, set the baud rate to 115200, and after power-on you can see the relevant serial port output. (Download a serial port tool yourself via Baidu, for example: sscom, xshell.)

  ![image-20250311144503520](../vendor/HiHope_NearLink_DK_WS63E_V03/doc/media/tools/image-20250311144503520.png)

## FAQ

- If compilation fails following the documentation, please refer to https://developers.hisilicon.com/postDetail?tid=02110170392979486020
- If compilation succeeds following the documentation, but fails after writing other code, you can post a question on the forum: https://developers.hisilicon.com/forum/0133146886267870001


    

  
