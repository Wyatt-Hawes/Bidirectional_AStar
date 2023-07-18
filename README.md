# Bidirectional_AStar
Implementation of a Bidirectional A* for pathfinding on a provided image


# Creating a Custom Map
Here’s how to create your own test map:
STEP 1: Find some image that you think will be easy to turn into a black-and-white occupancy map.
Save it as a PNG file. nm_interactive can only display PNG files.
ucsc_banana_slug-orig.png
STEP 2: In your favorite photo editor, create a black-and-white version (e.g. by desaturating and then
applying brightness and contrast operators). Save this in a lossless format like PNG.
ucsc_banana_slug.png
STEP 3: Run the navmesh builder program. You must have SciPy (http://www.scipy.org/) installed
for this program to work.
$ python nm_meshbuilder.py ucsc_banana_slug.png
Built a mesh with 711 boxes.
This will produce two files. The first is the mesh as a pickled Python data structure:
ucsc_banana_slug.png.mesh.pickle. The second is a visualization of the rectangular polygons extracted
by the navmesh builder:
STEP 4: Run your pathfinding program giving the original PNG file, the pickled mesh data, and some
subsampling factor. A factor of 1 displays the image at original size, while a factor of 4 will scale the
image down by a factor of four in each dimension for display (pathfinding will still be done at the full
resolution).
