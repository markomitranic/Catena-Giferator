# Catena Giferator
This project was created for Catena Media Serbia, as an easy way for designers to resize and optimize Gifs used in products.

## Usage
Application is dependency free, so it can be directly copied to your Applications folder.
Once you start the app, you can drag and drop any gif, image or video file, and it will automatically be compressed.
The gif will be output onto your Desktop, with a filename "output.gif". It will automatically overwrite older versions of the file if they exist.

## Compression

Compression algorhythm uses a few steps in order to make image smaller without changing the quality.
Via FFMPEG, static frames are made transparent, a color palette is calculated for each gif separately.
Both Gifsicle level 3 and ImageOptim are used for final compression and metadata removal.

Images are resized to 200x200 @ 20fps. Which is agreed upon standard for casino promotion GIFs.
If a need rises for another standard, you should contact the developer.