# Video_Frames_extraction
Extracting frames from a video

CODE :

<br><br>

import cv2<br>
vidcap = cv2.VideoCapture('VideoName.mp4')<br>
success, image = vidcap.read()<br>
count = 1600       #insert number of frames you want<br>
i = 0<br>
remaining_images = 50<br>
while True:<br>
    _, image = vidcap.read()   <br>
    if i >= count:   <br>
        cv2.imwrite("Frames/frame%d.jpg" % count, image)       # save frame as JPEG file   <br>
        count += 4 <br>
        print(i)  <br>
        remaining_images -= 1  <br>
    i += 1  <br>
    if remaining_images <= 0:  <br>
        break  <br>
