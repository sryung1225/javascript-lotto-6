# 과제 진행 📜

## 구현할 기능 목록

- [x] 로또 구입 금액 입력받기

  ```
  구입 금액을 입력해 주세요.
  4000
  ```

  - [x] 사용자가 잘못된 값을 입력할 경우 예외 발생 후 에러 메세지 출력
    - [x] 금액이 숫자가 아닌 경우
    - [x] 금액이 1,000원 이하일 경우
    - [x] 금액이 1,000원으로 나누어 떨어지지 않는 경우
    ```
    [ERROR] 구입 금액은 유효한 숫자여야 합니다.
    [ERROR] 구입 금액은 최소 로또 1장을 살 수 있어야 합니다.
    [ERROR] 구입 금액은 1,000원 단위여야 합니다.
    ```
  - [x] 제대로 입력 받을 때까지 반복 입력 받기

- [x] 로또 구매하기

  - [x] 구매한 로또 수량 출력 : 구입 금액 / 1000

  ```
  4개를 구매했습니다.
  ```

  - [x] 구매한 로또 번호 출력
    - [x] 1개의 로또 발행 마다 1-45 사이 중복 없는 랜덤 6개의 숫자 뽑기
    - [x] 로또의 각 번호는 오름차순 정렬

  ```
  [8, 21, 23, 41, 42, 43]
  [3, 5, 11, 16, 32, 38]
  [7, 11, 16, 35, 36, 44]
  [1, 8, 11, 31, 41, 42]
  ```

- [x] 당첨 번호 입력받기 : 쉼표를 기준으로 구분

  ```
  당첨 번호를 입력해 주세요.
  1,2,3,4,5,6
  ```

  - [x] 사용자가 잘못된 값을 입력할 경우 예외 발생 후 에러 메세지 출력
    - [x] 당첨 번호가 6개 미만이거나 초과인 경우
    - [x] 당첨 번호가 1-45 사이의 숫자가 아닌 경우
    - [x] 당첨 번호가 중복된 경우
    ```
    [ERROR] 로또 번호는 6개의 숫자여야 합니다.
    [ERROR] 로또 번호는 1부터 45 사이의 숫자여야 합니다.
    [ERROR] 로또 번호는 중복이 없어야 합니다.
    ```
  - [x] 제대로 입력 받을 때까지 반복 입력 받기

- [x] 보너스 번호 입력받기

  ```
  보너스 번호를 입력해 주세요.
  7
  ```

  - [x] 사용자가 잘못된 값을 입력할 경우 예외 발생 후 에러 메세지 출력
    - [x] 보너스 번호가 1-45 사이의 숫자가 아닌 경우
    - [x] 보너스 번호가 당첨 번호와 중복된 경우
    ```
    [ERROR] 로또 번호는 1부터 45 사이의 숫자여야 합니다.
    [ERROR] 로또 번호는 중복이 없어야 합니다.
    ```
  - [x] 제대로 입력 받을 때까지 반복 입력 받기

- [x] 당첨 내역 출력하기
  - [x] 구매한 로또 번호와 당첨 번호를 대조해서 일치한 번호의 수와 그 수량을 계산
  - [x] 수익률 계산
    - [x] 당첨 금액 / 구입 금액 \* 100
    - [x] 소수점 둘째 자리에서 반올림 (ex. 100.0%, 51.5%, 1,000,000,0%)
  - [x] 게임 종료
  ```
  당첨 통계
  ---
  3개 일치 (5,000원) - 1개
  4개 일치 (50,000원) - 0개
  5개 일치 (1,500,000원) - 0개
  5개 일치, 보너스 볼 일치 (30,000,000원) - 0개
  6개 일치 (2,000,000,000원) - 0개
  총 수익률은 62.5%입니다.
  ```

<br><br>

## 실행 결과 예시

```
구입금액을 입력해 주세요.
8000

8개를 구매했습니다.
[8, 21, 23, 41, 42, 43]
[3, 5, 11, 16, 32, 38]
[7, 11, 16, 35, 36, 44]
[1, 8, 11, 31, 41, 42]
[13, 14, 16, 38, 42, 45]
[7, 11, 30, 40, 42, 43]
[2, 13, 22, 32, 38, 45]
[1, 3, 5, 14, 22, 45]

당첨 번호를 입력해 주세요.
1,2,3,4,5,6

보너스 번호를 입력해 주세요.
7

당첨 통계
---
3개 일치 (5,000원) - 1개
4개 일치 (50,000원) - 0개
5개 일치 (1,500,000원) - 0개
5개 일치, 보너스 볼 일치 (30,000,000원) - 0개
6개 일치 (2,000,000,000원) - 0개
총 수익률은 62.5%입니다.
```

<br><br>

## 프로그래밍 요구 사항 확인 목록

- [x] Node.js 18.17.1 버전에 실행 가능해야 함
- [x] 프로그램 실행 시작점은 `App.js`의 `play` 메서드
  ```
  const app = new App();
  app.play();
  ```
- [x] [JavaScript 코드 컨벤션](https://github.com/woowacourse/woowacourse-docs/tree/main/styleguide/javascript)을 지키면서 프로그래밍
- [x] [커밋 메시지 컨벤션 가이드](https://gist.github.com/stephenparish/9941e89d80e2bc58a153)를 참고하여 기능 목록 단위로 커밋
- [ ] 프로그램 종료 시 `process.exit()`를 호출하지 않음
- [x] 프로그래밍 요구 사항에서 달리 명시하지 않는 한 파일, 패키지 이름 수정 및 이동 금지
- [x] indent depth를 2까지만 허용
- [x] 함수(또는 메서드)의 길이가 15라인을 넘어가지 않도록 구현. 한 가지 일만 잘 하도록
- [ ] else 사용을 지양
- [ ] Jest를 이용해서 기능이 정상 동작함을 테스트 코드로 확인
  - `__tests__/LottoTest.js` 를 참고하여 학습한 후 테스트 구현
  - 도메인 로직에 단위 테스트 구현
  - 단, UI(`Console.readLineAsync`, `Console.print`) 로직에 대한 단위 테스트는 제외
- [x] `@woowacourse/mission-utils`의 `Random` `Console` API를 사용해서 구현
  - 랜덤 값 추출을 위해 `Random.pickUniqueNumbersInRange()` 활용
  - 사용자 값 입력을 위해 `Console.readLineAsync` 활용
  - 출력을 위해 `Console.print` 활용
