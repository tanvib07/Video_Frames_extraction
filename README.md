# Video_Frames_extraction
Extracting frames from a video

CODE :

<br><br>

import cv2<br>
vidcap = cv2.VideoCapture('VideoName.mp4')<br>
success, image = vidcap.read()<br>
count = 1600      &emsp; #insert number of frames you want<br>
i = 0<br>
remaining_images = 50<br>
while True:<br>
    &emsp;_, image = vidcap.read()   <br>
    &emsp;if i >= count:   <br>
        &emsp;&emsp;cv2.imwrite("Frames/frame%d.jpg" % count, image)      &emsp; # save frame as JPEG file   <br>
        &emsp;&emsp;count += 4 <br>
        &emsp;&emsp;print(i)  <br>
        &emsp;&emsp;remaining_images -= 1  <br>
    &emsp;i += 1  <br>
    &emsp;if remaining_images <= 0:  <br>
        &emsp;&emsp;break  <br>
