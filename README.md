 

# MY IMAGE EDITOR



### ALL ABOUT IT...
This image editor is a web based image editor using Javascript. It is based on optimization of image processing and uses Cloudinary's client libraries (SDKs)(a cloud based service that provides end to end image management solution) which wrap the upload API and simplify integration with websites and mobile applications for image transformations. It supports basic image transformations like rotation, crop and undo. It works by uploading a given image on the cloudinary account. All the transformations are requested by calling their API through URL modifications. 

1) To use the editor, one must first of all have a cloudinary account. Use set_credentials function of the Cloudinary account where you want the transformations. It requires the cloud name, api_key and api_secret of your account. (For demo purpose, I have added my own personal credentials.)

2) Given a http link, upload() function would upload the image to the the Cloudinary account. (NOTE: The image that is to be uploaded must have a **http link** and not https.) 

3) Create_thumbnail will make a DOM object out of every new image given to it and add it to the image slider.(image-gallery)

4) Functionalities of rotateleft(), rotateright(), crop(), accept(), cancel(), undo() are provided.

                   a) rotateleft()- rotate the image 90 degrees anticlockwise.
                   
                   b) rotateright()- rotate the image 90 degrees clockwise.
                   
                   c) crop()- select a portion of the image.
                   
                   d) accept()- crop the selected area.
                   
                   e) cancel()- If you don't want to crop, and you want to deselect the selected area.
                   
                   f) undo()- This will take you one step back.(Note this will save just the previous image transformation,not all)
                   
The editor makes use of two seperate plugins- 1) imgareaselect for cropping and 2) lightslider-master for the image slider. 

### DEMO
Refer to **samplepopup.html**. The code contains proper documentation. (To get the editor without popup, refer to sample.html).

### DEPENDENCIES
All the required CSS and Javascript files are attached within the folder and commented out. In demo file, I have used the link of the files at our local server. (The path to the icons is also at our local server. One can modify it according to the path at their PC).

### HOW TO USE ?
Store all the images in imgArray and call create_thumbnail over the image link.Also upload the image on Cloudinary using upload() function. After the transformations, you can access the transformed images through the same array imgArray. (Note the transformed image would have an URL associated with the Cloudinary account).

### Customisation
You can customise the slider according to your need. All the defaults are mentioned in lightslider.js and can be modified according to the need. 
By default we have scaled all the images to 300px-300px to fit the width of the popup. This can be adjusted according to the need through modifying the height and width needed in 'scale' variable; 


### AND YOU ARE SET TO GO!!! 
