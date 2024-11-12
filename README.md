https://github.com/vinpple/jetson/blob/ed97161a1658e5609e6c8be0751ac17a3d1fd077/dxl1/main.cpp#L8-L9
ctrl+c를 입력하여 종료
https://github.com/vinpple/jetson/blob/ed97161a1658e5609e6c8be0751ac17a3d1fd077/dxl1/main.cpp#L11-L19
입력받은 왼쪽과 오른쪽 모터의 속도를 저장하고 실행 시간을 저장함
https://github.com/vinpple/jetson/blob/ed97161a1658e5609e6c8be0751ac17a3d1fd077/dxl1/main.cpp#L21-L34
왼쪽과 오른쪽 모터의 속도를 입력 받고 입력받은 속도로 모터의 속도를 설정 
usleep(20 * 1000); : 20ms 동안 대기
ctrl+c를 눌러 종료하면 실행 시간을 초 단위로 계산하여 출력한다.
