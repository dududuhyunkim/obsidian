# Duck typing

- 동적 타이핑의 한 종류로 객체의 변수 및 메소드의 집합이 객체의 타입을 결정하는 것을 말한다.
- 클래스 상속이나 인터페이스 구현으로 타입을 구분하는 것 대신, 객체가 어떤 타입에 걸맞은 변수와 메소드를 지니면 객체를 해당 타입에 속하는 것으로 간주한다.
  - "만약 어떤 새가 오리처럼 걷고, 헤엄치고, 꽥꽥거리는 소리를 낸다면 나는 그 새를 오리라고 부를 것이다."

```ts
class Duck {
  public quack() {
    console.log("Quaaaaaack!");
  }
  public feathers() {
    console.log("The duck has white and gray feathers.");
  }
}

class Person {
  public quack() {
    console.log("The person imitates a duck.");
  }
  public feathers() {
    console.log("The person takes a feather from the ground and shows it.");
  }
}

function inTheForest(duck: Duck) {
  duck.quack();
  duck.feathers();
}

function main() {
  const realDuck = new Duck();
  const personDuck = new Person();

  inTheForest(realDuck);
  inTheForest(personDuck);
}

```


reference
https://en.wikipedia.org/wiki/Duck_typing