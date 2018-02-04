# README

## Config

contains all the configurations for the app, your global config file, helper functions and navigation.

the folder structure can be something like:

´´´
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

´´´
Each component can have subcomponents like seen for the Slider component above. Let's say that the Slider component had become so complex, that it is more than 500 lines and you have lost the overview because there are too many different types of slider items. One way could be to break slider items into subcomponents for better overview. But these subcomponents they can't really go on the same level as the Slider component, because most likely you are not going to use a slider item outside of the slider component.


## Config

contains all the configurations for the app, your global config file, helper functions and navigation.

## Screens

contains all the configurations for the app, your global config file, helper functions and navigation.