# Code Convention

- 각자 의견을 나눠가며 지금 잘 맞는 규칙을 정합니다.
- 사소한 규칙도 기재하며 같이 만들어갑니다.
- 서로 일하기 좋은 컨벤션을 찾습니다.

#

## branch

### web

| 종류    | 사용패턴        | 특징                                           |
| :------ | :-------------- | :--------------------------------------------- |
| main    | main            | 상용 (프로덕션)                                |
| develop | develop         | 상용 배포 이전에 확인 가능한 브랜치 (스테이징) |
| feat    | feat/작업명     | [기능] dev에 병합                              |
| layout  | layout/페이지명 | [ 레이아웃] dev에 병합                         |
| fix     | fix/name        | [수정] dev에 병합                              |
| hotfix  | hotfix/name     | [hotfix] 메인에 병합                           |

### admin

| 종류    | 사용패턴                                              | 특징                                    |
| :------ | :---------------------------------------------------- | :-------------------------------------- |
| main    | main                                                  | 상용                                    |
| develop | develop                                               | 상용 배포 이전에 확인 가능한 dev 브랜치 |
| feature | feat/작업명                                             | develop에 병합                              |
| fix     | fix/작업명                                              | develop에 병합                              |
| hotfix  | hotfix/작업명                                           | main 병합                           |

## commit

## PR 형식

- PR 제목

```

```

```
## PR 타입(하나 이상의 PR 타입을 선택해주세요)
- [ ] 기능 추가
- [ ] 목업 페이지 구현
- [ ] CSS 수정
- [ ] 기능 삭제
- [ ] 버그 수정
- [ ] 의존성, 환경 변수, 빌드 관련 코드 업데이트
- [ ] 리팩토링

## 반영 브랜치
ex) feature/login -> dev

## 변경 사항
ex) 로그인 시, 구글 소셜 로그인 기능을 추가했습니다.

## 기타
ex) 추가된 라이브러리, 리뷰 요청 사항

```

## lint

## code

- 함수명과 구현체가 동일한 맥락으로 작성되어 있어야 한다.

### function naming

1. 컴포넌트 조작 함수 : handle + component + event 형태로 표현한다

```js
// bad
const onChange = () => {};
const onClick = () => {};

// good
const handleInputChange = () => {};
const handleSaveButtonClick = () => {};
```

2. 복수에 대한 네이밍 : list를 불러올 때에는 불러올 대상+s를 붙인 복수형으로 표현

```ts
// good
useOrder(); // 주문 상세 조회
useOrders(); // 주문 전체 조회 (배열 형태 응답)

// bad
useOrderList();
```

3. 약어 사용 자제, 부득이하게 약어가 필요하다고 판단되는 경우 팀원과의 상의 후 작성.

```ts
// bad
let arr;
let i;

// good
let array;
let index;
```

4. boolean형의 변수는 is,has 등을 붙여 의미를 명료하게 한다.

```ts
// bad
const editable;
// good
const isEditable;
```

5. 로컬 변수는 의미있는 단어를 선택한다.

```js
// bad
users.map((el) => el.name);

// good
users.map((user) => user.name);
```

## prettierrc

```ts
{
  "arrowParens": "always",
  "bracketSpacing": true,
  "htmlWhitespaceSensitivity": "css",
  "jsxBracketSameLine": false,
  "jsxSingleQuote": true,
  "printWidth": 80,
  "semi": true,
  "singleQuote": true,
  "tabWidth": 2,
  "trailingComma": "es5",
  "useTabs": false
}
```

## api interface

- endpoint 폴더
  - types.ts tpye정의
- 행위/end-point/Res or ReqParams

```ts
interface GetOrderRes {
  user: string;
}

interface CreateOrderReqParams {
  id: number;
}
```

### queryKey (react-query / tan-stack)

- 가독성을 위해 camelCase 사용
- 복수형 구분지어 사용하기

```ts
export const MAPPING = {
  KEY: "value",
};

// good
export const MAPPING = {
  key: "value",
};
```

### tsConfig

```ts
noImplicitAny: true;
```

#

### Reference

- https://evan-moon.github.io/2021/08/08/tsconfig-compiler-options-type-check/
- https://github.com/airbnb/javascript/#naming--uppercase
-
