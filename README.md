# fe-naming-rule

- 각자 의견을 나눠가며 지금 잘 맞는 규칙을 정합니다.
- 사소한 규칙도 기재하며 같이 만들어갑니다.
- 서로 일하기 좋은 컨벤션을 찾습니다.

#

### branch

### commit

### PR

### lint

### code

- 함수명과 구현체가 동일한 맥락으로 작성되어 있어야 한다.

### prettierrc

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

### api interface

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
