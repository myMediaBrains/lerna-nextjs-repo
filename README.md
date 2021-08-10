# [Building a NextJS Monorepo](https://javascript.plainenglish.io/building-a-nextjs-monorepo-ecd21ac04928)

## 프론트엔드 monorep 최소 requirements

| no   | 최소 requirements                                            |
| ---- | ------------------------------------------------------------ |
| 1    | (앱과 라이브러리를 contain) monorepo 에서 package 라는 용어를 사용하여 특정 코드 유닛을 구분한다. |
|      | package 는 an App 이 될 수도 있고, a shared module 이 될 수도 있다. |
|      | monorepo 에서는 /pacages/app/* 과 /pacakges/shared/* 로 각각 구분한다. |
| 2    | (bootstrap) CLI 명령을 사용하여 **새로운**  App 또는 **새로운** Shared Module 을 bootstrap 한다. |
| 3    | (test) **단 하나의 명령으로** monorepo 에서 **모든 테스트를 실행**한다. – 대안으로 App 또는 Shared Module 에서 각각 테스트를 실행할 수도 있다. |
| 4    | (Storybook) 프론트엔드 앱을 만드는 필수 요소이다.            |
|      | monorepop 에서 모든 stories 가 있는 **Storybook을 오픈**해야 한다. |
|      | 대안으로, 싱글 App 또는 Shared Module 에 있는 stories 만 가지는 Storybook 을 오픈할 수도 있다. |
| 5    | (Shared tooling config) ESLint, Prettier, TypeScript 의 구성에 대하여 개별 package 마다 반복할 필요가 없다. |
| 6    | (개별 빌드 스크립트) 개별 App 은 자신의 빌드 스크립트를 가진다. |
|      | App을 실행하는 스크립트들은 isolation 되어 있고, 또한 composition 을 할 수 있다. |
|      | 싱글 도메인에서 다른 paths 를 앱이 타겟팅하는 동시에, paths 를 실행하는 것을 composition 이라고 한다. (예제: /cutomer-dashboard/… 는 an Customer dashboard app 을 말하는 것이고, /back-office/… 는 administrative App 이다.) |

