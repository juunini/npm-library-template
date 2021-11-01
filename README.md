# NPM Library Template

[react-query](https://github.com/tannerlinsley/react-query) 의 레포지토리를 보고 참고했습니다.

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Babel](https://img.shields.io/badge/Babel-F9DC3E?style=for-the-badge&logo=babel&logoColor=white)
![Rollup](https://img.shields.io/badge/Rollup-F47521?style=for-the-badge&logoColor=white)

## dependencies

```sh
yarn add @babel/runtime react
```

## devDependencies

```sh
yarn add -D react-dom @types/react @types/react-dom @babel/cli @babel/core @babel/plugin-transform-runtime @babel/preset-env @babel/preset-react @babel/preset-typescript @babel/transform-runtime @rollup/plugin-replace @svgr/rollup babel-plugin-const-enum babel-plugin-transform-async-to-promises cross-env is-ci-cli replace rimraf rollup rollup-plugin-babel rollup-plugin-commonjs rollup-plugin-jscc rollup-plugin-node-resolve rollup-plugin-peer-deps-external rollup-plugin-size rollup-plugin-terser rollup-plugin-visualizer type-fest typescript
```

## 배포 전 테스트 하는 방법

`yarn build && yarn pack` 을 하면 `package.tgz` 파일이 생성됩니다.  
그 뒤 import 하여 테스트 할 프로젝트에서  

```sh
yarn add /Users/juunini/Desktop/your-project-name/package.tgz
```

같은 형식으로 로컬 설치를 하여 테스트 해볼 수 있습니다.

## 배포 하는 방법

먼저, [npm](https://www.npmjs.com/)에 가입해야 합니다.

`yarn npm login` 로 로그인을 한 뒤,  
`yarn npm publish --access=public` 로 배포합니다.

## 만약 같은 이름의 패키지가 존재해 prefix를 붙이고 싶을 때

`package.json` 의 `name` 필드에 prefix를 붙입니다.  
예를들어, `"name": "@juunini/react-checkbox"`

## 주의사항

`postinstall` scripts에는 의존성을 필요로 하는 무언가를 넣지 마세요.  
