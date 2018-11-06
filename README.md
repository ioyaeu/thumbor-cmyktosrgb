# thumbor-cmyktosrgb
A thumbor filter using icc profiles to convert from cmyk to rgb

Your thumbor version must have a PIL installed with icc profile management.

Add the python file into the filter directory located in thumbor.

Add to your thumbor confguration file : 
"'thumbor.filters.cmyktosrgb'," to the list of filters 
 
`############################## Color management ################################`
`# A path to directory containing ICC profiles.`
`ICC_PATH = '/usr/share/color/icc'` <- Put a real path
`# Name of the default ICC profile applied of none is specified.`
`ICC_FILE = 'CoatedFOGRA27.icc'` <- put a real file located in the path

restart your thumbor service

Example: http://<your thumbor>/unsafe/filters:cmyktosrgb()/some-cmyk-image.jpg