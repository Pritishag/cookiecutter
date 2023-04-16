#INITIAL SETUP
#----------------------------------------------------------------
import cv2
from cvzone import HandTrackingModule, overlayPNG
import numpy as np

intro = cv2.imread('frames/img1.png')
kill = cv2.imread('frames/img2.png')
winner = cv2.imread('frames/img3.png')
cam = cv2.VideoCapture(0)
detector = HandTrackingModule.HandDetector(maxHands=1,detectionCon=0.77)

#INITILIZING GAME COMPONENTS
#----------------------------------------------------------------
sqr_img = cv2.imread('img/sqr (1).png')
mlsa = cv2.imread('img/mlsa.png')

#INTRO SCREEN WILL STAY UNTIL Q IS PRESSED
gameOver = False
NotWon = True

#DISPLAY INTRO SCREEN
cv2.imshow("Intro Screen", intro)
cv2.waitKey(0)

#GAME LOGIC UPTO THE TEAMS
#-----------------------------------------------------------------------------------------
while not gameOver:
    continue

#LOSS SCREEN
if NotWon:
    for i in range(10):
        cv2.imshow("Loss Screen", kill)
        cv2.waitKey(1)

    while True:
        cv2.imshow("Loss Screen", kill)
        if cv2.waitKey(1) == ord('q'):
            break

else:
    #WIN SCREEN
    cv2.imshow("Win Screen", winner)

    while True:
        cv2.imshow("Win Screen", winner)
        if cv2.waitKey(1) == ord('q'):
            break

#DESTROY ALL WINDOWS
cv2.destroyAllWindows()
