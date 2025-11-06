# vue-demo

Vue3 기반 예제 컴포넌트 모음 (Composition API 사용)

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

개발 서버 실행 후 `http://localhost:8080` (또는 표시된 포트)에서 확인 가능합니다.

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

## 컴포넌트 구조

> **참고**: 각 컴포넌트를 확인하려면 `src/App.vue`에서 해당 컴포넌트를 import하여 사용하세요.  
> 개발 서버: `http://localhost:8080` (또는 표시된 포트)

### Example 1: 기본 인스턴스 및 바인딩
- **E-01-instance.vue**
  - 경로: `src/components/example1/E-01-instance.vue`
  - 설명: Vue 인스턴스 기본 사용법 (ref를 사용한 반응형 데이터)
  - 로컬 URL: `http://localhost:8080` (App.vue에서 현재 사용 중)

- **E-02-reactive.vue**
  - 경로: `src/components/example1/E-02-reactive.vue`
  - 설명: 반응형 데이터와 computed 속성, lifecycle hook (onMounted) 사용

- **E-03-binding.vue**
  - 경로: `src/components/example1/E-03-binding.vue`
  - 설명: v-model을 사용한 양방향 데이터 바인딩

### Example 2: 디렉티브
- **E-04-directives.vue**
  - 경로: `src/components/example2/E-04-directives.vue`
  - 설명: Vue 디렉티브 종합 예제
  - 기능: v-if, v-else-if, v-else, v-show, v-for, v-text, v-html, v-pre

### Example 3: 부모-자식 컴포넌트 통신
- **ParentComponent.vue**
  - 경로: `src/components/example3/ParentComponent.vue`
  - 설명: Props 전달 및 이벤트 수신

- **ChildComponent.vue**
  - 경로: `src/components/example3/ChildComponent.vue`
  - 설명: Props 수신 및 이벤트 emit (defineProps, defineEmits)

### Example 4: Provide/Inject
- **ParentComponent.vue**
  - 경로: `src/components/example4/ParentComponent.vue`
  - 설명: provide를 사용한 데이터 제공

- **ChildComponent1.vue**
  - 경로: `src/components/example4/ChildComponent1.vue`
  - 설명: inject를 사용한 데이터 주입 (자식 컴포넌트 포함)

- **ChildComponent2.vue**
  - 경로: `src/components/example4/ChildComponent2.vue`
  - 설명: inject를 사용한 데이터 주입

### Example 5: Options API vs Composition API
- **E-07-Options-API.vue**
  - 경로: `src/components/example5/E-07-Options-API.vue`
  - 설명: Options API 스타일 (비교용으로 유지)

- **E-08-composition-api.vue**
  - 경로: `src/components/example5/E-08-composition-api.vue`
  - 설명: Composition API (setup 함수) 스타일

- **E-09-composition-API2.vue**
  - 경로: `src/components/example5/E-09-composition-API2.vue`
  - 설명: `<script setup>` 문법 사용

### Example 6: ref와 reactive
- **E-10-ref.vue**
  - 경로: `src/components/example6/E-10-ref.vue`
  - 설명: ref를 사용한 원시 타입 반응형 데이터

- **E-11-reactive.vue**
  - 경로: `src/components/example6/E-11-reactive.vue`
  - 설명: reactive를 사용한 객체 반응형 데이터

- **E-12-ref-component.vue**
  - 경로: `src/components/example6/E-12-ref-component.vue`
  - 설명: ref를 사용한 DOM 요소 참조

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
