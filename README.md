# node-red-contrib-bbox-image
A custom Node-RED node to annotate the image with Object Detection bounding boxes.

## Installation

```
npm install node-red-contrib-bbox-image
```

## Usage
The `msg.payload` psssed to this node shall be an object and contains two
properties:
- image: the image data in Buffer data type.
- objects: an object array containing a list of detected objects.
  Each object has the following information:
  ```
  {
    bbox: [x, y, w, h],
    className: string,
    score: number
  }
  ```

This node annotates the bounding box of detected objects into the image and
sends to the next node as a Buffer.