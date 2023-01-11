> ### 🧡Dart 시작하기

> 어째서 다트인가?

왜 `다트`를 써야하나??

`다트`는 `google`에서 직접 개발한 언어로 편의에 따른 수정이 가능하다.

웹, 앱을 지원하는 하이브리드형 언어는 다양하지만, 예시로 `React-Native`는 `React`를 기반으로 작동하며 이는 `JavaScript`엔진을 사용하는데, 효율성을 개선하자고 `JavaScript`를 `Meta (전 FaceBook)`에서 뜯어고칠 순 없는것으로 설명이 된다.

> 어떻게 배워야 하는가?

![image](https://user-images.githubusercontent.com/46777310/211317379-e3f590f2-7bae-4755-bca4-0d43f4c4a8a6.png)

[DartPad](https://dartpad.dev/?)를 활용하여 온라인 컴파일러를 통한 개발을 진행하겠다. 설치해도 무관하나 실습을 위한 온라인 컴파일러도 충분하다.

> Hello World

![image](https://user-images.githubusercontent.com/46777310/211317952-da7760b5-ee46-43f8-9c0f-3d8c9b8e3cd0.png)

`Hello World`는 아래와 같이 출력하며 다른 언어와 같이 `main`함수에서 동작한다.

```dart
void main() {
  print("Hello World");
}

```

> Type

![image](https://user-images.githubusercontent.com/46777310/211319278-3afec31b-256c-4852-a557-94ff5e4b0053.png)

`Dart`의 `Type`지정은 매우 간단하다 `var` 혹은 `String`과 같은 타입 명시가 가능하며 `var`로 타입을 지정해도 `Dart`내부에서 타입을 인지하기 때문에 무엇으로 사용하던 큰 상관은 없다

```dart
void main() {
  var name = "Chobby!";
  name = "KimChobby!";
  String name2 = "Rony!";
  // Doesn't Work  name2 = (Int Value)
  print(name+name2);
}
```

> dynamic

두 번째로 `Dynamic`타입이 있는데, 해당 타입은 동적으로 변경되는 그 어떠한 타입도 수용한다는 의미로, 적극 추천되진 않지만 변수의 타입을 모르는 경우에 유용한 사용이 가능한 자료형이다.

```dart
void main() {
  dynamic name;
  name = 12;
  name = "Chobby";
  name = true;
  print(name); // Print true
}
```

> ?

세 번째로 `Nullable Variables`가 존재한다. 말 그대로 `null`을 허용하는 타입이란 의미이며, `null`타입은 종종 개발에 필요하기 때문에 이는 반드시 사용할 줄 알아야한다.

```dart
void main() {
  String? name = "Chobby"; // It Might String OR Null
  name = null;
  name?.isEmpty; // name? mean is not Null
  if(name is String) { // means not Null
    name.isNotEmpty;
  }
}
```

> final

`final`타입을 활용해 `JavaScript`의 `const`와 같은 상수를 선언할 수 있다. 해당 타입은 선언될 때만 변수에 값이 할당되며, 이후 타입, 값은 변경할 수 없다.

```dart
void main() {
  final name = "Chobby"; // === final String name = "Chobby";
  // name = 12; name is Constant Variable
  print(name);
}
```

> late

`late` 자료형은 다른 타입 앞에 선언되며, 변수를 임시로 등록만 하고 값은 이후에 할당한다는 의미로, 주로 `API`작업에 많이 활용된다.

```dart
void main() {
  late final String name;
  name = "Chobby"; // can assign String value
  print(name);
}
```

> const

`const`자료형은 `final`자료형과 같이 상수를 선언하고, 선언된 변수에는 다른 값을 할당할 수 없다.

```dart
void main() {
  const name = "chobby"; // like final
  name = 12; // Throw Error!
  print(name);
}
```

> 자료형들

`dart`의 자료형들이다.

```dart
void main() {
  String name = "Chobby"; // String
  bool flag = true; // boolean
  int age = 22; // integer
  double dollar = 3.99; // double
  num x = 12;
  x = 1.2; // integer OR double
}

```
