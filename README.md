# screen
screen 실행 방법

## download

- apt update
  
  ```bash
  sudo apt update
  ```

- screen 설치

  ```bash
  sudo apt install screen
  ```

## example

- screen 생성

  ```bash
  screen -S myjob
  ```

- screen 생성 로그 포함

  ```bash
  screen -L -S myjob
  ```

- 코드 실행

  ```bash
  python train.py
  ```

- 작업 확인

  ```bash
  screen -r myjob
  ```

- 작업 종료

  ```bash
  screen -S 1020 -X quit
  ```

  ```bash
  screen -S myjob -X quit
  ```

- 세션 빠져 나오기(종료 X)

  ```bash
  Ctrl + a → d
  ```
