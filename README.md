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

  ```bash
  screen -S myjob
  ```

  ```bash
  python train.py
  ```

  ```bash
  screen -r myjob
  ```

  ```bash
  screen -S 1020 -X quit
  ```
