<update(this file): 1/9/2018

# Adapt Avoidence nodes to fit OpenCV3
the original duckietown codes are likely to be written with Opencv2, there are some minor differnece you have to notice if you want to run 
them with OpenCV3


* ### prerequisites
* 1. get and compile the newest version of duckietown software on your computer

* ### How to do it?
* you need to modfy several pieces of source file.
* 1. static_object_detector_node.py [mdaop package], line 51, add an output to cv2.findContour function in the beginning of this line
 *   vehicle_detectin_node.py [vehicle_detection package], line 94, cv2.SimpleBlobDetector(params) ->> cv2.SimpleBlobDetector_create(params)
 *   ground_projection_node.py [ground_projection package], line 68, GetGroundCoordResponse(self.gp.pixel2ground(req.normalized_uv))
        ->>  GetGroundCoordResponse(self.gp.vector2ground(req.normalized_uv))
* then you are likely to successfully run obstacle and vehicle avoidance demo with OpenCV3
