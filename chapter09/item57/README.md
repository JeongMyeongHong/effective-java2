# [아이템 57] 지역변수의 범위를 최소화하라

## 요약

### 지역변수의 범위를 최소화하는 이유

- 코드 가독성과 유지 보수성을 높이고, 오류 가능성을 낮추기 위해
- `[아이템 15] 클래스 멤버의 접근 권한을 최소화하라` 와 비슷한 취지

### 최소화하는 방법

- 가장 처음 쓰일 떄 선언하라
- 지역변수를 선언과 동시에 초기화 하라
- 메서드를 작게 만들고, SRP 를 지켜라

## Tip

실수로 지역변수의 범위가 너무 넓다면 `{}` 로 감싸서 범위를 제한 할 수 있다.

```java
class Main {
    public static void main(String[] args) {
        {
            int i = 3;
        }
        System.out.print(i); // i의 접근이 불가능하다.
    }
}
```