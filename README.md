
Certainly! The provided Python code uses the OpenCV library to create a pencil sketch effect from an input image named "car.WEBP" and saves the result as "re.png". Here's a concise breakdown:

Read Image:
Load the input image ("car.WEBP") using cv2.imread().
image = cv2.imread("car.WEBP")

Convert to Grayscale:
Convert the color image to grayscale.

grey_img = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
Invert Grayscale Image:
Invert the grayscale image using cv2.bitwise_not().

invert = cv2.bitwise_not(grey_img)
Apply Gaussian Blur:
Apply Gaussian blur to the inverted image for smoothing.

blur = cv2.GaussianBlur(invert, (21, 21), 0)
Invert Blurred Image:
Invert the blurred image again.

invertedblur = cv2.bitwise_not(blur)
Create Pencil Sketch:
Generate the pencil sketch effect by dividing the grayscale image by the inverted blurred image using cv2.divide().

sketch = cv2.divide(grey_img, invertedblur, scale=256.0)
Save and Display Result:
Save the resulting sketch as "re.png" using cv2.imwrite() and display it using cv2.imshow().

cv2.imwrite("re.png", sketch)
cv2.imshow("pencil", sketch)

![Butterfly](https://github.com/git-prashanthkumar/PrashanthKumar/assets/162727418/5a994449-88eb-4cad-8ca2-ed07c6521920) ![re](https://github.com/git-prashanthkumar/PrashanthKumar/assets/162727418/275a6db1-d797-4b2f-8e4e-8d17197be188)



This code performs a series of image processing steps to create a pencil sketch effect and provides a visual representation of the result.
