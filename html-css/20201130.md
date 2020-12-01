# calc()안에서 SCSS 변수 사용하기 

[참고](https://stackoverflow.com/questions/17982111/sass-variable-in-css-calc-function)

## 문제 상황

SCSS 작업 중 공통된 수치들을 SCSS 변수로 처리하여 작업을 하고 있었는데 `calc()` 에서 작동하질 않았다.

## 해결

매우 간단하다. 변수에 `#{}`을 둘러준다.

```scss
// bad
.problem {
  width: calc(100% - $example);
}

// good
.problem {
  width: calc(100% - #{$example});
}
```

