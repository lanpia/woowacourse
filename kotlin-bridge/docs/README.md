### 기능목록
1. 다시 시작할때 처음에 만든 다리 재사용
2. 다리길이 세팅
3. 랜덤으로 갈 수 있는 장소와 없는 장소 설정
   - 랜덤값이 0인경우 아래칸이고 건널수 없는 칸
   - 1인경우 위칸이 건널수 있는칸
4. 사용자가 잘못된 값을 입력할 경우 IllegalArgumentException를 발생
   - "[ERROR]"로 시작하는 에러 메시지를 출력 후 
   - 그 부분부터 입력을 다시 받는다.

###입력 목록 - 올바른 값이 아닌 경우 모두 예외처리
1. 사용자에게 다리 길이 입력받는다.
        - 다리길이는 3이상 20이하
2. 사용자에게 이동할 칸을 입력받는다 
        - U & D
3. 게임 재시작 & 종료 여부를 입력 받는다.
        - R & Q

###출력 목록
1. "다리 건너기 게임을 시작합니다."
2. "이동할 칸을 선택해주세요.(위: U, 아래: D)"
3. "게임을 다시 시도할지 여부를 입력해주세요. (재시도: R, 종료: Q)"
4. "최종 게임 결과"
5. "게임 성공 여부 : 성공"
6. "총 시도한 횟수 : n"

### 게임 출력
[ O ]
[   ]

[ O | X ]
[   |   ]

[ O |   ]
[   | O ]

[ O |   |   ]
[   | O | O ]

1. 이동에 실패한 장소는 X 로 표시
2. 이동에 성공한 장소는 O로 표시
3. 이동하지 않은 칸은 공백으로 표시
4. 다리의 시작과 끝은 [  ] 로 표시
5. 다리 칸의 구분은 | 로 표시
6. 현재까지 건넌 다리를 모두 출력

###예외처리
1. 소문자 알파벳이 입력된 경우
2. 다리길이 입력시 숫자와 문자가 같이 입력된 경우
3. 다리길이 3~20 범위를 넘어선 값이 들어온 경우
4. 이동할 칸 입력시 소문자 u & d 가 입력된 경우
5. 재시도 여부 입력값이 잘못 된 경우