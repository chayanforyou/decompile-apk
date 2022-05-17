# Compile, decompile and sign APK using apktool utility.

1. Download latest [apktool](https://ibotpeaches.github.io/Apktool/install) version.
2. Download the [wrapper script](https://github.com/iBotPeaches/Apktool/tree/master/scripts).
3. Create a folder anywhere in the PC and put both files (`apktool.jar` & `apktool.bat`) in that folder.

4. Open command prompt.
5. Navigate to the folder where you placed `apktool.jar`, wrapper script and the `apktool.bat`.
6. Now, you need to install the file using the " IF " command.
7. Type the following command.

```powershell
apktool if name-of-the-app.apk`
```

8. For decompiling use the command "d". The "d" stands for decompile.

```powershell
apktool d name-of-the-app.apk
```
  
9. After the app is correctly decompiled, a new folder will be created in the same folder where you placed your app. This contains all the xml's and smali files which can be edited for different mode's.

10. To recompile the app use the following command " B ". The "b" simply means recompile.

```powershell
apktool b name-of-the-app-folder
```

11. The final modded app will be in the `dist` folder located inside the original app folder created by apktool.

## Signing the apk

1. Open a new command prompt and change into the sign-apk directory using cmd
2. Move the modified-unsigned apk into this folder

3. Then type the following command -

```powershell
java -jar signapk.jar certificate.pem key.pk8 path-of-the-folder-contaning-the-apk.apk path-of-the-new-signed-apk.apk
```
	
4. Once compiled, the signed apk will be found in the same folder.

## Zipalign

1. Open command prompt.
2. Type the following command.

```powershell
zipalign -fv 4 semcmusic_signed.apk semcmusic_signed_zipaligned.apk
```
