# Autonomous-Field-Robotics
Following is the breakdown of this project:

Image Replacement with Homography:

Goal: Replace a picture in image1 with image2 using a computed Homography matrix (H).
Approach:
Select four corner points in both images to calculate H.
Apply the computed H to map every pixel from image2 onto image1.
Note: Use Python, matplotlib.pyplot for point selection, and cv2.warpPerspective for pixel mapping.
Over-Constrained Homography Calculation:

Objective: Determine the impact of using 8 points instead of 4 to compute the Homography matrix (H) for image mapping.
Method:
Choose an additional 4 points in both images.
Recompute H with 8 points.
Compare the differences in the H matrix.
Map a new image onto image1 using the updated H.
Note: Maintain Python code in a notebook and use cv2.findHomography for both 4-point and 8-point calculations.
Outdoor Image Mosaic with Homography:

Goal: Create a panoramic mosaic from multiple overlapping outdoor images.
Procedure:
Capture five overlapping images by rotating the camera.
Hand-pick common points in each image.
Compute Homographies for mapping images onto each other.
Blend the images for a seamless panorama.
Hint: Start with the center image as image 0 and map homographies from center to outer images.
Additional Information: Research and implement blending techniques, considering Burt and Adelson's classic paper for insight.
