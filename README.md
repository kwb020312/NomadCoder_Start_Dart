> ### π§‘Dart μμνκΈ°

> μ΄μ§Έμ λ€νΈμΈκ°?

μ `λ€νΈ`λ₯Ό μ¨μΌνλ??

`λ€νΈ`λ `google`μμ μ§μ  κ°λ°ν μΈμ΄λ‘ νΈμμ λ°λ₯Έ μμ μ΄ κ°λ₯νλ€.

μΉ, μ±μ μ§μνλ νμ΄λΈλ¦¬λν μΈμ΄λ λ€μνμ§λ§, μμλ‘ `React-Native`λ `React`λ₯Ό κΈ°λ°μΌλ‘ μλνλ©° μ΄λ `JavaScript`μμ§μ μ¬μ©νλλ°, ν¨μ¨μ±μ κ°μ νμκ³  `JavaScript`λ₯Ό `Meta (μ  FaceBook)`μμ λ―μ΄κ³ μΉ  μ μλκ²μΌλ‘ μ€λͺμ΄ λλ€.

> μ΄λ»κ² λ°°μμΌ νλκ°?

![image](https://user-images.githubusercontent.com/46777310/211317379-e3f590f2-7bae-4755-bca4-0d43f4c4a8a6.png)

[DartPad](https://dartpad.dev/?)λ₯Ό νμ©νμ¬ μ¨λΌμΈ μ»΄νμΌλ¬λ₯Ό ν΅ν κ°λ°μ μ§ννκ² λ€. μ€μΉν΄λ λ¬΄κ΄νλ μ€μ΅μ μν μ¨λΌμΈ μ»΄νμΌλ¬λ μΆ©λΆνλ€.

> Hello World

![image](https://user-images.githubusercontent.com/46777310/211317952-da7760b5-ee46-43f8-9c0f-3d8c9b8e3cd0.png)

`Hello World`λ μλμ κ°μ΄ μΆλ ₯νλ©° λ€λ₯Έ μΈμ΄μ κ°μ΄ `main`ν¨μμμ λμνλ€.

```dart
void main() {
  print("Hello World");
}

```

> Type

![image](https://user-images.githubusercontent.com/46777310/211319278-3afec31b-256c-4852-a557-94ff5e4b0053.png)

`Dart`μ `Type`μ§μ μ λ§€μ° κ°λ¨νλ€ `var` νΉμ `String`κ³Ό κ°μ νμ λͺμκ° κ°λ₯νλ©° `var`λ‘ νμμ μ§μ ν΄λ `Dart`λ΄λΆμμ νμμ μΈμ§νκΈ° λλ¬Έμ λ¬΄μμΌλ‘ μ¬μ©νλ ν° μκ΄μ μλ€

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

λ λ²μ§Έλ‘ `Dynamic`νμμ΄ μλλ°, ν΄λΉ νμμ λμ μΌλ‘ λ³κ²½λλ κ·Έ μ΄λ ν νμλ μμ©νλ€λ μλ―Έλ‘, μ κ·Ή μΆμ²λμ§ μμ§λ§ λ³μμ νμμ λͺ¨λ₯΄λ κ²½μ°μ μ μ©ν μ¬μ©μ΄ κ°λ₯ν μλ£νμ΄λ€.

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

μΈ λ²μ§Έλ‘ `Nullable Variables`κ° μ‘΄μ¬νλ€. λ§ κ·Έλλ‘ `null`μ νμ©νλ νμμ΄λ μλ―Έμ΄λ©°, `null`νμμ μ’μ’ κ°λ°μ νμνκΈ° λλ¬Έμ μ΄λ λ°λμ μ¬μ©ν  μ€ μμμΌνλ€.

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

`final`νμμ νμ©ν΄ `JavaScript`μ `const`μ κ°μ μμλ₯Ό μ μΈν  μ μλ€. ν΄λΉ νμμ μ μΈλ  λλ§ λ³μμ κ°μ΄ ν λΉλλ©°, μ΄ν νμ, κ°μ λ³κ²½ν  μ μλ€.

```dart
void main() {
  final name = "Chobby"; // === final String name = "Chobby";
  // name = 12; name is Constant Variable
  print(name);
}
```

> late

`late` μλ£νμ λ€λ₯Έ νμ μμ μ μΈλλ©°, λ³μλ₯Ό μμλ‘ λ±λ‘λ§ νκ³  κ°μ μ΄νμ ν λΉνλ€λ μλ―Έλ‘, μ£Όλ‘ `API`μμμ λ§μ΄ νμ©λλ€.

```dart
void main() {
  late final String name;
  name = "Chobby"; // can assign String value
  print(name);
}
```

> const

`const`μλ£νμ `final`μλ£νκ³Ό κ°μ΄ μμλ₯Ό μ μΈνκ³ , μ μΈλ λ³μμλ λ€λ₯Έ κ°μ ν λΉν  μ μλ€.

```dart
void main() {
  const name = "chobby"; // like final
  name = 12; // Throw Error!
  print(name);
}
```

> μλ£νλ€

`dart`μ μλ£νλ€μ΄λ€.

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
