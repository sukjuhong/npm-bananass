# 설치하기 {#installation}

이번 챕터에서는 바나나 프레임워크를 설치하는 두 가지 상세한 방법에 대해 소개합니다!

---

[[TOC]]

## 선행 설치 사항 {#prerequisites}

바나나 프레임워크는 [LTS<sup>Long Term Support</sup>](https://ko.wikipedia.org/wiki/%EC%9E%A5%EA%B8%B0_%EC%A7%80%EC%9B%90_%EB%B2%84%EC%A0%84) 및 최신 버전의 Node.js에서 동작하며, [Git](https://git-scm.com/)을 필요로 합니다! 아직 Node.js 및 Git을 설치하지 않았다면 아래 가이드를 참고해주세요.

### Node.js {#nodejs}

바나나 프레임워크는 `^20.18.0 || ^22.3.0 || >= 24.0.0` 범위에 해당하는 Node.js에서 동작합니다. (`v21`등 최신이 아닌 홀수 버전은 공식 지원하지 않습니다.)

아직 Node.js를 설치하지 않았다면, [Node.js 공식 홈페이지](https://nodejs.org/)에서 가능한 최신 LTS 버전을 설치해주세요.

::: info 주목해주세요!

바나나 프레임워크는 내부적으로 짝수 번호로 시작하는 LTS 버전 및 최신 버전(홀수 버전 포함)의 Node.js에 대해서만 테스트를 진행합니다! 안정적인 환경에서의 사용을 위해 최신 LTS 버전을 사용하는 것을 권장합니다.

:::

설치 후, 아래 명령어를 터미널에 입력하여 Node.js가 정상 설치되었는지 확인해주세요.

- 입력

    ```sh
    $ node -v
    ```

- 올바른 출력 예시

    ```sh
    v20.18.0
    ```

### Git {#git}

아직 Git을 설치하지 않았다면, [Git 공식 홈페이지](https://git-scm.com/)에서 가능한 최신 버전을 설치해주세요.

설치 후, 아래 명령어를 터미널에 입력하여 Git이 정상 설치되었는지 확인해주세요.

- 입력

    ```sh
    $ git -v
    ```

- 올바른 출력 예시

    ```sh
    git version 2.46.0
    ```

설치가 모두 완료되었나요? 그럼 이제 바나나 프레임워크를 설치해봅시다!

## `create-bananass`로 시작하기 {#getting-started-with-create-bananass}

가장 빠르게 바나나 프레임워크를 만나는 방법은 `create-bananass` 명령어를 이용하는 것입니다!

[React](https://ko.react.dev)의 <code>create-react-app</code>, [Next.js](https://nextjs.org)의 <code>create-next-app</code>처럼 <code>create-bananass</code>를 통해 지금 바로 바나나 프레임워크를 시작할 수 있습니다. 이 명령어는 바나나 프레임워크를 위한 프로젝트 템플릿을 생성합니다.

아래 명령어 중 하나를 터미널(CLI)에 입력해 `create-bananass`를 실행해주세요!

::: code-group

```sh [npm]
$ npx create-bananass@latest
# 또는
$ npm create bananass@latest
# 또는
$ npm init bananass@latest
```

:::

::: warning 주의하세요!

`create-bananass`는 아직 `yarn` 및 `pnpm` 등 `npm` 이외의 패키지 매니저를 지원하지 않습니다. 반드시 `npm`을 사용해주세요.

추가로, `yarn` 및 `pnpm` 등의 패키지 매니저를 이용하실 계획이 있으시다면, 하단의 [직접 설치해서 시작하기](#getting-started-with-manual-installation)를 참고해주세요.

:::

::: details 더 알아보기: `create-bananass` 명령어는 어떤 과정을 거쳐 프로젝트를 생성하나요?

`create-bananass` 명령어는 아래와 같은 일을 수행합니다.

1. 사용자의 입력을 받아 프로젝트 템플릿을 결정합니다.
1. 자바스크립트 또는 타입스크립트 템플릿을 복사하여 프로젝트 디렉토리를 생성합니다.
1. Visual Studio Code를 위한 확장 프로그램을 설치합니다.
1. `git init` 명령어를 실행하여 Git 저장소를 초기화합니다.
1. `npm install` 명령어를 실행하여 의존성을 설치합니다.

템플릿 복사를 제외한 모든 과정은 선택적이며, CLI(터미널, 콘솔)에 옵션 인자를 전달하여 **생략할 수 있습니다**. 자세한 내용은 [`create-bananass` CLI 문서](../learn/other-useful-cli-commands.md#create-bananass)를 참고해주세요.

:::

만약, 아래와 같은 메시지가 출력된다면, 키보드에서 `y` 키를 누르고 `Enter`를 눌러주세요. (`0.1.0`에 해당하는 패키지 버전은 달라질 수 있습니다.)

```sh
Need to install the following packages:
create-bananass@0.1.0
Ok to proceed? (y)
```

다음으로, 아래와 같은 질문에 답해주세요. 답변에 따라 바나나 프레임워크의 구성 및 설정이 달라집니다!

`○ Yes / ● No`의 경우, 키보드 화살표와 `Enter` 혹은 `y` 또는 `n` 키를 눌러 선택할 수 있습니다.

```sh
❯ Which directory should this project be located in?
.

❯ Would you like to use CommonJS module system?
○ Yes / ● No

❯ Would you like to use TypeScript?
○ Yes / ● No

❯ Would you like to skip initializing Visual Studio Code configurations?
○ Yes / ● No

❯ Would you like to skip initializing Git?
○ Yes / ● No

❯ Would you like to skip installing packages with npm?
○ Yes / ● No
```

모든 선택을 완료하면, 지정한 폴더에 자동으로 바나나 프레임워크 프로젝트가 생성되며, 성공적으로 설치하였을 경우 아래와 같은 메시지가 출력됩니다.

```sh
✓ Successfully created a new Bananass framework project!
```

## 직접 설치해서 시작하기 {#getting-started-with-manual-installation}

<!-- @include: @/shared/wip.ko.md -->
