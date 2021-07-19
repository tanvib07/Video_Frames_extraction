# Video_Frames_extraction
Extracting frames from a video

CODE :

import cv2
vidcap = cv2.VideoCapture('VideoName.mp4')
success, image = vidcap.read()
count = 1600       #insert number of frames you want
i = 0
remaining_images = 50
while True:
    _, image = vidcap.read()
    if i >= count:
        cv2.imwrite("Frames/frame%d.jpg" % count, image)       # save frame as JPEG file
        count += 4
        print(i)
        remaining_images -= 1
    i += 1
    if remaining_images <= 0:
        break
