# 3주차 로또

## 구현할 기능 목록

1. 로또 구입 금액 입력
    1. `구입금액을 입력해 주세요.`
    2. 유효성 검사 `예외 처리`
        1. 숫자를 입력했는지
        2. 1,000원 단위로 입력하였는지 (1,000원으로 나누어 떨어지지 않을 경우)
       3. 1,000원 미만의 숫자를 입력하였을 경우
2. 입력된 구입 금액에 따른 구입 개수와 복권 출력
    1. `0개를 구매했습니다.`
    2. 로또 번호는 1 ~ 45의 범위
    3. 하나의 로또당 중복되지 않는 6개의 숫자
    4. 로또 번호는 오름차순으로 정렬하여 출력

    ```
    [8, 21, 23, 41, 42, 43]
    [3, 5, 11, 16, 32, 38]
    [7, 11, 16, 35, 36, 44]
    [1, 8, 11, 31, 41, 42]
    [13, 14, 16, 38, 42, 45]
    [7, 11, 30, 40, 42, 43]
    [2, 13, 22, 32, 38, 45]
    [1, 3, 5, 14, 22, 45]
    ```

3. 당첨 번호 입력받기
    1. 쉼표를 기준으로 구분하여 입력받음
    2. 보너스 번호는 별도로 안내 후 입력
    3. 유효성 검사
        1. 쉼표를 기준으로 구분하였는지?
        2. 6개의 숫자를 입력하였는지?
        3. 중복된 숫자는 없는지?
        4. 1부터 45 사이의 숫자가 맞는지?
        5. 보너스 번호는 하나의 숫자만 입력하였는지? 
4. 당첨 결과 안내
    1. 하나의 로또당 일치하는 숫자 개수 출력 (당첨 내역)
    2. 수익률 출력 (소수점 둘째 자리에서 출력)


## 요구 사항

1. 함수(또는 메서드)의 길이가 15라인을 넘어가지 않도록 구현한다.
    - 함수(또는 메서드)가 한 가지 일만 잘 하도록 구현한다.
2. else 예약어를 쓰지 않는다.
    - 힌트: if 조건절에서 값을 return하는 방식으로 구현하면 else를 사용하지 않아도 된다.
    - else를 쓰지 말라고 하니 switch/case로 구현하는 경우가 있는데 switch/case도 허용하지 않는다.
3. Java Enum 사용
4. 도메인 로직에 단위 테스트 구현해야 한다. 단, UI(System.out, System.in, Scanner) 로직은 제외한다.
    - 핵심 로직을 구현하는 코드와 UI를 담당하는 로직을 분리해 구현한다.
    - 단위 테스트 작성이 익숙하지 않다면 `test/java/lotto/LottoTest`를 참고하여 학습한 후 테스트를 구현한다.
5. 사용자가 잘못된 값을 입력할 경우 `IllegalArgumentException`를 발생시키고, "[ERROR]"로 시작하는 에러 메시지를 출력 후 그 부분부터 입력을 다시 받는다.
    - `Exception`이 아닌 `IllegalArgumentException`, `IllegalStateException` 등과 같은 명확한 유형을 처리한다.