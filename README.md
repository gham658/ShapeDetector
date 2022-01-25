## ShapeDetector
# Reads and labels shapes from an image using OpenCV

This is a python project using OpenCV to detect and label shapes from an image. The stackImages function allows the program to stack images horizontally and vertically to display what is happening each step. 

There are a total of 5 images displayed (plus 1 placeholder) when the program is complete, the first is the raw image being given to the program and is unedited. The next 3 are all slightly changes using OpenCV, with one being turned to black and white, then the next a slight blur to smooth the edges, and a canny to find the edges. Before the final image shows the image after the getContours function runs

getContours is responsible for the primary motive of this program, using OpenCV, it detects and returns all of the contours that it finds on the entire image, drawing them over the edges of the shapes. Next, the funtion gets an approximation of how many points the contour drew, and this is used to determine which shape was observed 3 points is triangle, 4 is square/rectangle, and >4 is a circle. Squares and rectangles are differentiated by a quick aspect ratio calculation to see how close to 1 they are. Finally the program will write whatever shape the object corresponds to on the shape.
