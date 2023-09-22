# Project Title: Homography-Based Image Manipulation and Panorama Creation

## Image Replacement with Homography:

**Goal:**  
Replace a picture in `image1` with `image2` using a computed Homography matrix (H).

**Approach:**  
1. Select four corner points in both images to calculate H.
2. Apply the computed H to map every pixel from `image2` onto `image1`.

**Implementation Notes:**  
- Utilize Python and `matplotlib.pyplot` for point selection.
- Use `cv2.warpPerspective` for pixel mapping.

## Over-Constrained Homography Calculation:

**Objective:**  
Determine the impact of using 8 points instead of 4 to compute the Homography matrix (H) for image mapping.

**Method:**  
1. Choose an additional 4 points in both images.
2. Recompute H with 8 points.
3. Compare the differences in the H matrix.
4. Map a new image onto `image1` using the updated H.

**Implementation Notes:**  
- Maintain Python code in a notebook.
- Use `cv2.findHomography` for both 4-point and 8-point calculations.

## Outdoor Image Mosaic with Homography:

**Goal:**  
Create a panoramic mosaic from multiple overlapping outdoor images.

**Procedure:**  
1. Capture five overlapping images by rotating the camera.
2. Hand-pick common points in each image.
3. Compute Homographies for mapping images onto each other.
4. Blend the images for a seamless panorama.

**Useful Tips:**  
- Start with the center image as image 0 and map homographies from center to outer images.
- Research and implement blending techniques, considering insights from Burt and Adelson's classic paper for reference.
