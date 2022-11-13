English | [繁體中文](README_TCH.md)
# Ngrok-in-StableDiffusion-tutorial
A tutorial for enable ngrok in stable diffusion

## Why you need to enable Ngrok in stable diffusion
Ngrok can help you generate a public url for sharing your stable diffusion webui for other device.
## [Tutorial Video](https://youtu.be/Dgcz315UjbM)
You can click the image below to watch the [tutorial video](https://youtu.be/Dgcz315UjbM).

<a href="http://www.youtube.com/watch?feature=player_embedded&v=Dgcz315UjbM" target="_blank">
 <img src="http://img.youtube.com/vi/Dgcz315UjbM/mqdefault.jpg" alt="Watch the video"/>
</a>

## How to enable Ngrok in stable diffusion webui
### Windows user
* edit your ```webui-user.bat```

* get the [authtoken from ngrok](https://dashboard.ngrok.com/get-started/your-authtoken). If you don't have ngrok account you can register [here](https://ngrok.com/).
  * ![authtoken](sample/authtoken.png)

---
## There are two way to open Ngrok.

if you want only share url and don't need account system for protecting

* add ```COMMANDLINE_ARGS=--ngrok authtoken```
  * ![sample](sample/auth_only.png)

if you need account system use this

* add ```COMMANDLINE_ARGS=--ngrok authtoken:username:password```
  * ![pw](sample/pw.png)
---
* After edit and save bat file. Just run the bat. Remeber to use the latest ngrok.py to run it successfully.
  * if it successfully activate it will show this.
    * ![success](sample/ngrok_hint.png)
    * you can get public url here.
  * if you failed may see this.
    * ![fail](sample/fail.png)
    * pleaze check if you use the latest verion of [ngrok.py](modules/ngrok.py). Or the right format of ```COMMANDLINE_ARGS=--ngrok authtoken:username:password```. Or use the wrong authtoken.
    
* If you successfully activate. Open the url it gave you.
 * you will see this page. Press visit site to enter.
 * ![page](sample/page.png)
   * If you had set an account you will see this.
   * ![pw](sample/page_pw.png)
   * You will need to enter the right ```username``` and ```password``` to enter. If you can only see a blank page just refresh the page to clear cache.
* At the end. You can see the Stable diffusion webui page and use it. 
 * ![sd](sample/sd.png)
## Why I want to make this tutorial
There are few info for teaching how to activate this to share url in webui document. And my [ppull request](https://github.com/AUTOMATIC1111/stable-diffusion-webui/pull/4563) about ngrok in [stable-diffusion-webui](https://github.com/AUTOMATIC1111/stable-diffusion-webui) has been approved by [AUTOMATIC1111](https://github.com/AUTOMATIC1111). 

That is my honor to merge my code into such big project. It is a shame for no body use the feature I edit so I made this tutorial to help you use it.

![merge](sample/merge.png)
