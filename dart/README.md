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
- switch case

#### 반복문
- for (int i = 0; i < 10; i++)
- while (true)
- break, continue

#### 함수
- 함수 문법

    ```dart
    calc(int x, [int y = 10, int z = 15]) {
        int sum = x + y + z;

        print('x : $x, y : $y, z : $z');

        if (sum % 2 == 0) {
            print('짝수');
        } else {
            print('홀수');
        }
    }

    calc({
        required int x,
        required int y,
        required int z,
    }) { 
        ...
    }

    void main() {
        calc(z : 22, y : 11, x : 33);
    }
    ```

- 람다 방식

    ```dart
    typedef Operation = int Function(int x, int y, int z);

    int add(int x, int y, int z) => x + y + z;
    int subtract(int x, int y, int z) => x - y - z;

    int calculate(int x, int y, int z, Operation operation) {
        return operation(x, y, z);
    }

    Operation op = add;

    int result= op(5, 6, 7);

    int result2 = calculate(4, 5, 6, add);  
    ```

### 객체지향

#### 클래스
- Person 클래스

    ```dart
    // person.dart
    class Person {
        String name;
        int age;

        // 기본 생성자
        Person(this.name, this.age);

        // named constructor
        Person.anonymous() : name = 'Anonymous', age = 0;

        void sayHello() {
            print('안녕, 나는 $name, $age 살이야.');
        }

        @override
        String toString() => 'Person(name: $name, age: $age)';
    }

    void main() {
        var p1 = Person('지우', 28);
        var p2 = Person.anonymous();
        p1.sayHello();
        print(p2);
    }
    ```

#### 중급 객체지향은 패스


### 함수형

#### 함수형 프로그래밍

- Map 사용

    ```dart
    Map<String, int> superHeros = {
        'Ironman': 900,
        'Thor': 1300,
        'Spiderman': 850
    };

    final result = superHeros.map(
        (key, value) => MapEntry(
            'Marvel Hero $key',
            'Power $value',
        ),
    );

    final keys = superHeros.keys.map((x) => 'Marvel $x').toList();
    final values = superHeros.values.map((x) => 'Power $x').toList();

    ```

- Set 동일
- 컬렉션 호환

    ```dart
    List<Map<String, int>> heros = [
    {
        'Ironman': 900,
        'Group': 0, // 0 means Marvel
    },
    {
        'Superman': 2600,
        'Group': 1, // 1 means DC
    },
    {'Black Widow': 500, 'Group': 0},
    ];

    print(heros);
    print(heros.where((x) => x['Group'] == 0));
    ```

- .toList() 로 리스트화 


- reduce()

    ```dart
    List<int> numbers = [1,2,3,4,5,6,7];

    final result = numbers.reduce((prev, next) {
        print('--------------');
        print('prev : $prev');
        print('next : $next');

        return prev + next;
    });

    print(result);
    ```

- fold() ...

    - TO BE Continued...



### 비동기 프로그래밍

#### Future

- 미래에 받아올 값

    ```dart
    
    ```