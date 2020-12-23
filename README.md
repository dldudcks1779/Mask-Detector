<div>
  <p align="center">
    <img width="500" src="result_video.gif"> 
  </p>
</div>

## 마스크 착용 유무 판단 시스템
* ### 학습 dataset 생성
<div>
  <p align="center">
    <img width="500" src="image1.png"> 
  </p>
</div>


  * ##### caffemodel 파일 : 얼굴 인식을 위해 ResNet 기본 네트워크를 사용하는 SSD(Single Shot Detector) 프레임워크를 통해 사전 훈련된 모델 가중치 사용
    * ##### ResNet : https://blog.naver.com/dldudcks1779/222112744384
  * ##### prototxt 파일 : 모델의 레이어 구성 및 속성 정의

---
### 실행 환경
* #### Ubuntu
* #### OpenCV Version : 3.x.x
  * ##### 설치 : https://blog.naver.com/dldudcks1779/222020005648
* #### imutils
  * ##### 설치 : sudo pip3 install imutils
  
---
## 이미지 얼굴 인식
* #### 이미지를 저장하지 않을 경우
  * sudo python3 face_detection_image.py --input 이미지 경로
    * 예) sudo python3 face_detection_image.py --input ./face_image.jpg
* #### 이미지를 저장할 경우
  * sudo python3 face_detection_image.py --input 이미지 경로 --output 저장할 이미지 경로
    * 예) sudo python3 face_detection_image.py --input ./face_image.jpg --output ./result_face_image.jpg

<div>
  <p align="center">
    <img width="300" src="face_image.jpg"> 
    <img width="300" src="result_face_image.jpg">
  </p>
</div>

---
## 비디오 얼굴 인식 - 웹캠 또는 동영상(webcam or video)
* #### 비디오를 저장하지 않을 경우
  * webcam : sudo python3 face_detection_video.py
    * 예) sudo python3 face_detection_video.py
  * video : sudo python3 face_detection_video.py --input 비디오 경로
    * 예) sudo python3 face_detection_video.py --input ./face_video.avi
* #### 비디오를 저장할 경우
  * webcam : sudo python3 face_detection_video.py --output 저장할 비디오 경로
    * 예) sudo python3 face_detection_video.py --output ./result_face_video.avi
  * video : sudo python3 face_detection_video.py --input 비디오 경로 --output 저장할 비디오 경로
    * 예) sudo python3 face_detection_video.py --input ./face_video.avi --output ./result_face_video.avi

---
