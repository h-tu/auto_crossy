# auto_crossy

I'm training an AI to play crossy road the computer game with CNN. 

Inspired by [sendtex's gta project](https://github.com/Sentdex/pygta5)

![game_img](https://images.squarespace-cdn.com/content/v1/5cedd5e7c6e7df0001bbb67c/1564551904738-KZM0F360MGS6LSD6ZXTB/ke17ZwdGBToddI8pDm48kGwqNa-TSATgABi909OK27Z7gQa3H78H3Y0txjaiv_0fDoOvxcdMmMKkDsyUqMSsMWxHk725yiiHCCLfrh8O1z5QPOohDIaIeljMHgDF5CVlOqpeNLcJ80NK65_fV7S1UQSxQa_pE67Ig1CszvlZo11NCLvqIlshiNC_JCcjnOmqOV4zqrbdg_2AqIEjj1Z3Fg/Screenshot_Banner_01.jpg?format=1500w)

## Get started

As the name suggests, the code in grab_data takes care of the part where all the training datas are collected. The code's default running environment should be a working 'crossy road' app running on the top left corner, windowed, at 666 * 1280. The code will grab a snapshot about 10 times per second and processes it a little bit before saving each coresponding folder related to the action linked to the image, within the '/data' folder under the current working directory. This code also offers a functionality that allows you to clear all saved images under '/data', with all folders indicating motions untouched. 

More about image processing part:



[Crossy Road](https://www.crossyroad.com/)
