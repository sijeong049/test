작성일 : 2019.07.09
작성 내용 : online fall detection system

실행 환경
os : ubuntu 16.04
cuda : 8.0
cuDNN : 5.1

필요 선행 설치
 1. cuda, cuDNN
 2. OpenPose (설치 방법 : https://github.com/CMU-Perceptual-Computing-Lab/openpose/blob/master/doc/installation.md)

실행 순서
1. client(raspberry pi)
 - /home/pi/fall_detection/stream_test/img_stream_stream_client3.py 
  (실행 명령어 : python 파일이 있는 경로에서 python img_stream_client3.py)
  
2. server(pc)
 2.1 img_server
   - /home/fall_detection_online/test/img_cap_server.py 
    (실행 명령어 : python 파일이 있는 경로에서 python img_cap_server.py)
    ** 절대 경로로 잡혀있는 폴더들 경로 수정 필요
    
 2.2 OpenPose (설치 경로 예시 /home/openpose)
   - /home/openpose/2D_rgb_video_inference.sh
    (shell 실행 명령어 : shell 파일이 있는 경로에서 ./2D_rgb_video_inference.sh)
   - 
   
 2.3 fall_detection_online 폴더
