# Setup Windows without a Microsoft Account

Microsoft forces a Microsoft account when setting up Windows. In builds of Windows 11 starting with 25H2, the `OOBE\BypassNRO` workaround no longer exists, due to Microsoft removing the script file that added the necessary registry keys to perform this.

!!! note
	While the BypassNRO script required the lack of a network connection for the bypass to work, this new workflow, as of 25H2, **currently** does not require a lack of internet connectivity to function. This may change in the future.

1. When OOBE launches, press `Shift + F10` to open a command prompt window.

	!!! info
		On some computers, the function keys default to media keys, requiring the use of the `Fn` key being held to trigger the function layer. If the function keys aren't `F1` through `F12` as the primary function, you'll want to use `Shift + Fn + F10`.

2. Within the command prompt window, type `start ms-cxh:localonly` and press `Enter`.
3. In the window that pops up, Enter the display name, and optionally a password for the new user.
4. On most prebuilt PCs with factory customized images (HP, Lenovo, etc.), there's an additional screen asking for data collection. You can uncheck all of the boxes, or click **Skip** at this prompt.
5. Continue setup as normal, unchecking all of the permissions, and following the rest of OOBE as was done in Windows 10 and earlier builds of Windows 11.