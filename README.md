## Tools:
This repo contains a series of tools and application guides to drive the **T5UIC1** DWIN display that comes with some 3d  printers like: _**Creality Ender 3 V2**_ or _**Voxelab Aquila**_. This type of display is controlled by another mcu through a series of serial instructions described in the **Kernel Application Guide** document. The current version of the **Ender 3 V2** display kernel is **v2.0** but the dwin website only has the v1.2 in english. However, I've found the chinese version for v2.0 and used an online transaltor to translate it to english. Both versions are provided.

While browsing through the dwin dev forum I found a series of tools for this type of display:  

* **SSCOM - Serial Debugging tool** - A tool to communicate with serial devices. You need to know the hex instrucions to handshake and control the display (you can find tehm inside aplication guide document).
	<details>
	  <summary>📷 Screenshot!</summary>

	![alt text](https://github.com/ihrapsa/T5UIC1_DWIN_toolset/blob/main/img/sscom.png)

	</details> 

* **Tool for T5UIC1** - Contains all the necessary tools to communicate with the display, create `.ICO` files, upload/create `HZK` fonts, edit the `.cfg` file and some other. The GUI facilitates some steps that you'd have to manually do with the sscom. 
 
	<details>
	  <summary>📷 Screenshots!</summary>
	
	Device Config:  	
	![alt text](https://github.com/ihrapsa/T5UIC1_DWIN_toolset/blob/main/img/Tool_For_T5UIC1.png)

	ICO Tool:
	![alt text](https://github.com/ihrapsa/T5UIC1_DWIN_toolset/blob/main/img/T5UIC1_ico.png)

	Command Control:
	![alt text](https://github.com/ihrapsa/T5UIC1_DWIN_toolset/blob/main/img/T5UIC1_commmand_control.png)

	</details>

* **DWIN ToolBox** - Contains a series of tools (some are included in the Tool for T5UIC1 as well) but this is not exclusivly designed for T5UIC1  
	<details>
	  <summary>📷 Screenshot!</summary>

	![alt text](https://github.com/ihrapsa/T5UIC1_DWIN_toolset/blob/main/img/DWIN_tool_box.png)

	</details>

* **dwin-ico-tools** - Tool created by [b-pub](https://github.com/b-pub/dwin-ico-tools) to pack and unpack `9.ICO` files. Check his [README.md](https://github.com/b-pub/dwin-ico-tools/blob/main/README.md) for how to use it	

## Links:  

### **Tools & docs**
- http://forum.dwin.com.cn/ - DWIN dev forum. You need to create an account to download attatchments. 95% in chinese - use a Google Transalte extension to translate the webpages  
	Some T5UIC1 related threads:  
	- http://forum.dwin.com.cn/forum.php?mod=viewthread&tid=571&extra=page%3D1  
	- http://forum.dwin.com.cn/forum.php?mod=viewthread&tid=3012&extra=page%3D1  
- http://www.dwin.com.cn/service/en/file/id/13 DWIN website where some tools and documentation can be downloaded from
- http://www.ampdisplay.com/download1.php?cat=HMI%20UART(DWIN)&sub_cat=DGUS - AMP display website - DWIN related tools and docs
- https://github.com/b-pub/dwin-ico-tools tool to pack and unpack `9.ICO` files	

### **Klipper:** 

- [odwdinc](https://github.com/odwdinc/DWIN_T5UIC1_LCD)'s Python class to drive the display through Rpi's GPIO and Octoprint API  
 https://github.com/odwdinc/DWIN_T5UIC1_LCD  

- [Desuuuu](https://github.com/Desuuuu/klipper)'s klipper fork:works for T5UID1 DWIN displays. The display stays connected to the mainboard.  
https://github.com/Desuuuu/klipper  
https://github.com/KevinOConnor/klipper/compare/master...Desuuuu:master - comparison between this fork and origin.  
	
- Klipper TFT PRs
BTT 24/35 encoder serial (SPI) TFT that emulates a st7920 LCD:  https://github.com/KevinOConnor/klipper/issues/2231 
Prusa mini+ encoder serial (SPI) TFT: https://github.com/KevinOConnor/klipper/pull/4374

### **Marlin**

_Marlin ExtUI tweaks:_

- Jyers: https://github.com/Jyers/Marlin/wiki
- mriscoc: https://github.com/mriscoc/Marlin_Ender3v2/releases/tag/2.0.9.X
- otiss: https://otioss.com/posts/ender3-v2-front-panel  

_Marlin UI PRs_
- The Eg: https://github.com/MarlinFirmware/Marlin/pull/22211
- thinkyhead: https://github.com/MarlinFirmware/Marlin/pull/19371
- animations: https://github.com/MarlinFirmware/Marlin/pull/19395
	
	
