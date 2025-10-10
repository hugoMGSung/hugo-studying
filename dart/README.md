## Futter/Dart 학습

### 웹사이트 학습이 적절
- Android Studio 에서 모바일 프로젝트로 Dart 학습은 부적절
- https://dartpad.dev/ 에서 학습할 것

### 기본 문법
- Dart 기본 코드 : Dartpad 사이트 처음 소스코드

    ```dart
    void main() {
        for (var i = 0; i < 10; i++) {
            print('hello ${i + 1}');
        }
    }
    ```

- 기본은

    ```dart
    void main() {
        // TO DO ...
    }
    ```

#### 기본 출력
- 기본 출력 방법
    ```dart
    void main() {
        print('헬로, 다트!');
    }
    ```

    ![alt text](image.png)

#### 변수
- var 키워드 사용

    ```dart
    void main() {
        // 주석
        var name = '다트';

        print('헬로, ' + name + '!');
    }
    ```

#### 데이터 타입
- 문자형
    - String
    - ${} : 문자열 템플릿, 포맷팅에 사용
- 숫자형
    - int, double, num
- 불린형
    - bool
- 동적형
    - dynamic
- nullable 
    - 타입형?
- 타입확인
    - 변수.runtimeType
- final : 한번 선언후 변경 불가
- 날짜형
    - DateTime
    - DateTime.now()
- 바이트 데이터\
    - ByteData

#### 자료형 변환
- toInt(), toDouble()
- toString(), double.parse()

#### 연산자
- 기본 연산자 : + - * / % ++ -- 
- 대입 연산자 : = += -= *= /= 
- 널 연산자 : ??= 
- 조건 연산자 : > < >= <= == !=
- 타입 연산자 : is, is!

#### 컬렉션
- List

    ```dart
    List<String> superHeros = ['아이언맨', '토르', '스파이더맨'];
    print(superHeros);
    ```

- List 연산자
    - index : `[]`
    - length
    - add, remove, indexOf

- Map

    ```dart
    Map<String, int> heroVals = {
        'Ironman': 900,
        'Thor': 1200,
        'Spiderman': 840
    }
    ```

- Set...

#### 조건문
- if () else if () else () 

#### 반복문

