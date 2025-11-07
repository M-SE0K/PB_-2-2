# vue-demo
**초급프로젝트 실습 2-2**

Vue2를 Vue3 변환

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

개발 서버 실행 후 `http://localhost:8080` (또는 터미널에 표시된 포트)에서 확인 가능합니다.

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

## 컴포넌트 구조

> **참고**: 각 컴포넌트를 확인하려면 `src/App.vue`에서 해당 컴포넌트의 주석을 해제하여 확인하세요.
> 편의를 위해 `<div>`태그를 이용하였습니다.
>
> 개발 서버: `http://localhost:8080` (또는 표시된 포트)

### Example 1: 기본 인스턴스 및 바인딩
- **E-01-instance.vue**
  - ![example1-E01](./img/example1/example1_instance.png)
- **E-02-reactive.vue**
  - ![example1-EO2](./img/example1/example1_reactive.png)
- **E-03-binding.vue**
  - ![example1-E03](./img/example1/example1_binding1.png)
  - ![example1-E03](./img/example1/example1_binding2.png)
### Example 2: 디렉티브
- **E-04-directives.vue**
  - ![example2-E04](./img/example2/example2_directives.png)

### Example 3: 부모-자식 컴포넌트 통신
- **ParentComponent.vue**
  - ![example3-E04](./img/example3/example3_parent-child.png)

- **ChildComponent.vue**
  - 경로: `src/components/example3/ChildComponent.vue`
  - ![example3-E04](./img/example3/example3_childComponent.png)

### Example 4: Provide/Inject
- **ParentComponent.vue**
  - ![example5-parentComponent](./img/example4/example4_parent-child.png)

- **ChildComponent1.vue**
  - ![example4-childComponent](./img/example4/example4_childComponent1.png)

- **ChildComponent2.vue**
  - ![example4-childComponent](./img/example4/example4_childComponent2.png)

### Example 5: Options API vs Composition API
- **E-07-Options-API.vue**
  - ![example5-Options](./img/example5/example5_optionsAPI1.png)
  - ![example5-Options](./img/example5/example5_optionsAPI2.png)
  - ![example5-Options](./img/example5/example5_optionsAPI3.png)

- **E-08-composition-api.vue**
  - ![example5-CompositiconAPI](./img/example5/example5_compositionAPI1.png)
  - ![example5-CompositiconAPI](./img/example5/example5_compositionAPI2.png)
  - ![example5-CompositiconAPI](./img/example5/example5_compositionAPI3.png)
- **E-09-composition-API2.vue**
  - ![example5-CompositiconAPI2](./img/example5/example5_compositionAPI2_1.png)
  - ![example5-CompositiconAPI2](./img/example5/example5_compositionAPI2_2.png)
  - ![example5-CompositiconAPI2](./img/example5/example5_compositionAPI2_3.png)
### Example 6: ref와 reactive
- **E-10-ref.vue**
  - ![example6-ref](./img/example6/example6_ref1.png)
  - ![example6-ref](./img/example6/example6_ref2.png)
  - ![example6-ref](./img/example6/example6_ref3.png)

- **E-11-reactive.vue**
  - ![example6-reactive](./img/example6/example6_reactive1.png)
  - ![example6-reactive](./img/example6/example6_reactive2.png)

- **E-12-ref-component.vue**
  - ![example6-ref-component](./img/example6/example6_ref_component1.png)
  - ![example6-ref-component](./img/example6/example6_ref_component2.png)


## 주요 변경 사항 (Vue2 → Vue3)

모든 컴포넌트는 Vue3의 Composition API (`<script setup>`)로 작성되었습니다:
- Options API → Composition API
- `data()` → `ref()` / `reactive()`
- `computed` → `computed()`
- `methods` → 일반 함수
- `mounted()` → `onMounted()`
- `beforeUnmount()` → `onBeforeUnmount()`
- `$emit` → `defineEmits()`
- `provide/inject` → `provide()` / `inject()` 함수

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
