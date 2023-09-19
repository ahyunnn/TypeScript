## [TypeScript] 1. 타입스크립트 소개와 배경

by.  [캡틴판교](https://joshua1988.github.io/ts/why-ts.html#%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8%EB%9E%80)

#### 1. 타입스크립트?

* 자바스크립트에 타입을 부여한 언어 -> 자바스크립트의 확장된 언어

* 타입스크립트는 브라우저에서 실행하기 위해 파일을 한 번 컴파일해주어야 함

#### 2. why 타입스크립트?

* 에러의 사전 방지 
  
  * 의도하지 않은 코드의 동작을 예방할 수 있음
    
    ```javascript
    // math.js
    function sum(a, b) {
        return a + b;
    }
    
    console.log(sum(10, 20)); // 30
    console.log(sum(10, '20')); // 1020
    ```
    
    ```typescript
    // math.ts
    function sum(a: number, b: number) {
        return a + b;
    }
    
    console.log(sum(10, 20)); // 30
    console.log(sum(10, '20')); // Error
    ```

* 코드 자동 완성과 가이드
  
  * 타입스크립트를 사용하면 개발 툴의 기능을 최대로 활용할 수 있음
  
  * VSCode에서 해당 타입에 대한 API를 미리 보기로 띄워주고, tab으로 빠르고 정확하게 작성할 수 있음
