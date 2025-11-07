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

### 컴포넌트별 변경 요약
- `E-01-instance.vue`: 기본 인스턴스 예제를 `<script setup>`으로 변환하고 `ref`를 이용해 초기 데이터를 선언했습니다.
- `E-02-reactive.vue`: `reactive` 객체를 활용해 복합 상태를 구성하고, Vue2 `data` 속성을 대체했습니다.
- `E-03-binding.vue`: 양방향/단방향 바인딩을 `ref`와 `computed` 조합으로 재구성했습니다.
- `E-04-directives.vue`: 디렉티브 예제를 Composition API 함수와 템플릿 기준 문법으로 정리했습니다.
- `ParentComponent.vue` (`example3`): 부모 상태를 `ref`로 정의하고 자식에게 `props`와 이벤트를 전달하도록 업데이트했습니다.
- `ChildComponent.vue` (`example3`): `defineProps`와 `defineEmits`로 메시지 전달과 커스텀 이벤트 전송을 구현했습니다.
- `ParentComponent.vue` (`example4`): `provide`로 공유 데이터를 전달하도록 Composition API 기반으로 수정했습니다.
- `ChildComponent1.vue` (`example4`): `inject`를 사용해 부모의 제공 데이터를 수신하도록 구현했습니다.
- `ChildComponent2.vue` (`example4`): 다중 주입 데이터를 읽고 내부 상태로 활용하도록 구성했습니다.
- `E-07-Options-API.vue`: Options API 예제를 Composition API와 나란히 비교할 수 있도록 `<script setup>` 구조로 정리했습니다.
- `E-08-composition-api.vue`: Composition API 패턴을 `ref`, `computed`, `watch` 등으로 정리해 Options API 대비 장점을 보여줍니다.
- `E-09-composition-API2.vue`: Composition API 확장 예제로 훅 분리와 재사용 가능 로직 작성법을 시연합니다.
- `E-10-ref.vue`: 여러 `ref` 활용법과 DOM 참조 사용법을 Vue3 스타일로 변환했습니다.
- `E-11-reactive.vue`: `reactive` 상태와 `toRefs` 변환을 통해 반응형 객체를 관리합니다.
- `E-12-ref-component.vue`: `ref`를 활용한 자식 컴포넌트 참조 및 메서드 호출 패턴을 구현했습니다.

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
