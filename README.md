# Digital Circlism
It is a modern artistic expression in which paintings are made with digital tools usually featuring celebrities made of thousands of flat circles on a black background.
# Project Overview
Using traditional method for circlism is time consuming but using algorithms we can save that time.
This project consists of a algorithmic artwork. It is designed to apply digital circlism to images within 10 minutes or less depending upon image resolution.

These are some outputs of our project.

<img src="./images/input/cart.jpg" width="400px"><img src="./images/output/cartoon_out.png"  width="400px">

<img src="./images/input/minion.jpg"  width="400px"><img src="./images/output/minion_out.png"  width="400px">

<img src="./images/input/leaf.jpg"  width="400px"><img src="./images/output/leaf_out.png"  width="400px">

## Steps for Project accomplishment:

1. Input Image
2. Image Segmentation using Mean Shift Filtering
3. Canny Edge Detection
4. Some Image Filtering to reduce noise
5. Euclidean Distance Transform of each pixel
6. Background Separation 
7. Closed Circle Packing with Circles of different denominations

## Algorithm for Circle Packing:
Deciding set of denomiations to get circles of variable denomination.Let this be stored in set D in decending order.
```
bool isOccupied[n][m]={false} // where n and m are the size of the image and initialise all pixel to false
## Input image = I;
for each radius in D:
  for each pixel in I:
    if EDT(p) >= radius && isOccupied[pixel] == False:
      C = Circle(center=p, radius=EDT(p)
      if isOccupied[each pixel within the circle range] == False:
      
        ## set each pixel in range of circle to True in order to overcome overlapping condition
        isOccupied[for all points in C] = True
        DrawCircle(C)
```
Worst-case complexity for this algorithm is O(n²k), where n is total number of pixels constituting the image and k is the size of denomination set.
