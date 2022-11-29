# custom_font_matplotlib_add
This repository holds a file with instructions on how to add custom fonts to matplotlib

The main reference comes from this article: https://towardsdatascience.com/how-to-use-custom-fonts-with-matplotlib-in-5-minutes-or-less-57c63ece2a11

Essentially, download and unzip the files. Then use matplotlib.font_manager to add the fonts to the system then can be used with font family. 

Minimal example: 
import matplotlib.font_manager as font_manager

# Add every font at the specified location
font_dir = ['/Users/darioradecic/Downloads/Merriweather']
for font in font_manager.findSystemFonts(font_dir):
    font_manager.fontManager.addfont(font)

# Set font family globally
rcParams['font.family'] = 'Merriweather'
