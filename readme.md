# README

## Basic folder structure

    /app
        /components
        /config
        /screens

## Components

Contains all the components that are used in other components or in the screens:

    /components
        /Button
            /Button.js

        /Slider
            /Slider.js
            /components
                /ImageItem
                    /ImageItem.js
                /TextItem
                    /TextItem.js

Each component can have subcomponents, as seen for the Slider component above. 
Let's say that the Slider component has become so complex that it had more than 500 lines, and you have lost overview because there are too many different types of slider items. One way to deal with this could be to move the slider items into subcomponents for better overview. Why subcomponents? Well, in this case these slider-item components don't really work on the same level as the Slider component, because it is not very likely that you are going to use a slider item outside of the slider component. 
However, there will be cases where it would make sense to have those two on the same outerlevel.


## Config

Contains all the configurations for the app, your global config file, helper functions and navigation.

    /config
        /routes.js
        /helpers.js
        /env.js
        
There are no rules, but if you are working with something that is not a component, like a helper function or a global environment configuration, then you can add them there.


## Screens

Here you define all the screens in the app, with their subcomponents.

    /screens
        /Home
            /Home.js
        /Profile
            /Profile.js
            /components
                /PictureUploader
                    /PictureUploader.js
        /Settings
            /Settings.js
            
If a screen contains some components that are very specific for the screen, and you know that they won't be used on any other screen, then it can be a good idea to place them there, like the PictureUploader for the Profile. One advantage of doing so is that, if you change something in a subcomponent, then you know that you only need to adjust it in the parent screen. For example, in the PictureUploader case above, you would only need to change the Profile screen. In addition, there is no doubt where the component is used. 
