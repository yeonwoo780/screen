# Background 실행방법

- [Ubuntu](#screen)
- [Window](#Start)

## screen
screen 실행 방법 (Ubuntu)

### download

- apt update
  
  ```bash
  sudo apt update
  ```

- screen 설치

  ```bash
  sudo apt install screen
  ```

### example

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

---

## Start

start 실행 방법 (Window)

### Example

- python 작업 확인

  ```bash
  Get-Process python* |
  Select-Object Id, ProcessName, Path
  ```

- 시작

  ```bash
  Start-Process uv `
    -ArgumentList "run app.py" `
    -WindowStyle Hidden
  ```

- process 종료

  ```bash
  Stop-Process -Id 19620 -Force
  ```

- python으로 돌아가고 있는거 중에서 경로가 ~인거 종료

  ```bash
  Get-Process python |
  Where-Object {
      $_.Path -like "*\AppData\Roaming\uv\python\*"
  } |
  Stop-Process -Force
  ```
