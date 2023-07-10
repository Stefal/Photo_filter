# Photo_filter

Filter photo sequences
```
usage: photo_filter.py [-h] [-d DUPLICATE_DISTANCE] [-j JSON_FILE] [-r]
                       [-t MAX_TURN_ANGLE] [-e ENCLOSING_IMAGES] [-v]
                       paths [paths ...]

 - Search for distance based duplicate images and move them in a 'duplicate' subfolder.
 - Search for image in geofence zones and move them in a 'geofence' subfolder
 - Search for images with a too large angle between them.

positional arguments:
  paths                 paths to the images folders

optional arguments:
  -h, --help            show this help message and exit
  -d DUPLICATE_DISTANCE, --duplicate_distance DUPLICATE_DISTANCE
                        Min distance in meter for duplicate image detection.
                        Default: 0.5 meter(s)
  -j JSON_FILE, --json_file JSON_FILE
                        Path to the geojson file containing geofence polygons
  -r, --recursive       search images in subdirectory
  -t MAX_TURN_ANGLE, --max_turn_angle MAX_TURN_ANGLE
                        Check if two subsequent images have a too large direction angle.
                        The result will be send to Josm as an image layer.
                        Default: False°
  -e ENCLOSING_IMAGES, --enclosing_images ENCLOSING_IMAGES
                        Set how many images will be added around a too tight angle. These images will be included in the Josm session.
                         Exemple with 10: 2 images before and 8 images after.
                        Default: 10 images
  -v, --version         show program's version number and exit
```
## installation:

+ Create a virtual environnement: `python3 -m venv photo_filter`
+ Move to this environnement: `cd photo_filter`
+ Activate this environnement: linux: `source bin/activate` - windows powershell:  `bin\script\activate.ps1`
+ Clone this repository: `git clone https://github.com/Stefal/Photo_filter.git`
+ Install the requirements: `pip install -r Photo_filter/requirements.txt`