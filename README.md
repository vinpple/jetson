https://github.com/vinpple/jetson/blob/ed97161a1658e5609e6c8be0751ac17a3d1fd077/dxl1/main.cpp#L8-L9
ctrl+c를 입력하여 종료
https://github.com/vinpple/jetson/blob/ed97161a1658e5609e6c8be0751ac17a3d1fd077/dxl1/main.cpp#L11-L19
입력받은 왼쪽과 오른쪽 모터의 속도를 저장하고 실행 시간을 저장함
https://github.com/vinpple/jetson/blob/ed97161a1658e5609e6c8be0751ac17a3d1fd077/dxl1/main.cpp#L21-L34
왼쪽과 오른쪽 모터의 속도를 입력 받고 입력받은 속도로 모터의 속도를 설정 

usleep(20 * 1000); : 20ms 동안 대기

ctrl+c를 눌러 종료하면 실행 시간을 초 단위로 계산하여 출력한다.

Ctrl+c를 누르면 바로 종료하지 않고 명령을 한번 더 입력하면 종료하는데 이유를 설명하라. 이걸 해결하려면 어떻게 해야 하는지 나중에 생각해볼 것

cin으로 입력을 기다리는 동안 SIGINT 신호를 처리하지 못합니다. Ctrl+C를 눌러도 입력 대기 상태에서 신호가 누적되고, 그 후 cin을 통해 입력을 받으면 신호 처리 (ctrl_c_pressed = true)가 이루어지고, 그 후 루프를 종료하는 방식입니다.

