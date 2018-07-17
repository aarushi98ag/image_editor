 

# MY IMAGE EDITOR



### ALL ABOUT IT...
This image editor is a web based image editor using Javascript. It is based on optimization of image processing and uses Cloudinary's client libraries (SDKs)(a cloud based service that provides end to end image management solution) which wrap the upload API and simplify integration with websites and mobile applications for image transformations. It supports basic image transformations like rotation, crop and undo. It works by uploading a given image on the cloudinary account. All the transformations are requested by calling their API through URL modifications. 

1) To use the editor, one must first of all have a cloudinary account. Use set_credentials function of the Cloudinary account where you want the transformations. It requires the cloud name, api_key and api_secret of your account.

2) Given a http link, getURl function would upload the image to the the Cloudinary account.

3) Create_thumbnail will make a DOM object out of every new image given to it and add it to the image slider.(image-gallery)

4) Functionalities of rotateleft(), rotateright(), crop(), accept(), cancel(), undo() are provided.

The editor makes use of two seperate plugins- 1) imgareaselect for cropping and 2) lightslider-master for the image slider. 

### DEMO
Refer to samplepopup.html. The code contains proper documentation. 

### DEPENDENCIES
All the required CSS and Javascript files are attached within the folder and commented out. In demo file, I have used the link of the files at our local server. 

### HOW TO USE ?
Store all the images in imgArray and call create_thumbnail over the image link. After the transformations, you can access the transformed images through the same array imgArray. (Note the transformed image would have an URL associated with the Cloudinary account).

### Customisation
You can customise the slider according to your need. All the defaults are mentioned in lightslider.js and can be modified according to the need. 
By default we have scaled all the images to 300px-300px to fit the width of the popup. This can be adjusted according to the need.


### AND YOU ARE SET TO GO!!! 
