## [TypeScript] 3. 변수와 함수 타입 정의하기

by.  [캡틴판교](https://joshua1988.github.io/ts/why-ts.html#%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8%EB%9E%80)



#### 1.  문자열

```typescript
let str: string = 'hello';
```

#### 2. 숫자

```typescript
let num: number = 10;
```

#### 3. 배열

```typescript
let arr: Array<number> = [1, 2, 3];
let heroes: Array<string> = ['capt', 'thor', 'hulk'];
let items: number[] = [1, 2, 3]; // 배열 리터럴 사용
```

#### 4. 튜플 : 배열의 각각 인덱스에 타입 지정

```typescript
let address: [string, number] = ['city', 10];
```

#### 5. 객체

```typescript
let obj: object = {};
let person: object = {
    name: 'lee',
    age: 100
};
let person1: {name: string, age: number} = {
    name: 'ahyun',
    age: 1000
};
```

#### 6. 진위값

```typescript
let show: boolean = true;
```

#### 7. 함수

* 함수의 파라미터에 타입 지정이 가능함 (1대 1 매핑)

* 파라미터를 제한할 수 있음

* 옵셔널 파라미터를 통해 파라미터를 선택적으로 쓸 수 있음

```typescript
// 함수에 타입을 정의하는 방식
function sum(a: number, b: number): number {
    return a + b;
}

// 옵셔널 파라미터
function log(a: string, b?: string) {}


log('hello world'); // 파라미터를 하나 생략해도 error가 뜨지 않는다. 
log('hello ts', 'abc');
```
