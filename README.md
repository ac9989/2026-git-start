# 2026-git-start

로컬에서 추가한 내용입니다!
github 웹에서 추가한 내용입니다


오늘의 학습 목표: 작업자 B의 Merge 충돌 실습

오늘의 학습 목표: Git 협업 이해
오늘의 학습 목표: 작업자 A의 Git 협업 실습


# README.md 작성 및 Markdown 활용 실습

## 실습 과정 시퀀스 다이어그램

```mermaid
sequenceDiagram
    autonumber

    actor 사용자
    participant README as README.md
    participant MD as Markdown
    participant Emoji as 이모지
    participant GitHub as GitHub

    Note over 사용자,README: 1. README.md 파일 작성

    사용자->>README: README.md 생성
    사용자->>README: 프로젝트 목적 작성
    사용자->>README: 주요 기능 작성
    사용자->>README: 설치 방법 작성
    사용자->>README: 사용 방법 작성
    README-->>사용자: 프로젝트 안내 문서 완성

    Note over 사용자,MD: 2. Markdown 기본 문법 적용

    사용자->>MD: 제목 문법 작성
    MD-->>README: 제목 적용

    사용자->>MD: 강조 문법 작성
    MD-->>README: 굵게 / 기울임 / 취소선 / 코드 적용

    사용자->>MD: 목록 문법 작성
    MD-->>README: 순서 있는 목록 / 순서 없는 목록 적용

    사용자->>MD: 링크 작성
    MD-->>README: 링크 적용

    사용자->>MD: 이미지 작성
    MD-->>README: 이미지 적용

    사용자->>MD: 인용문 작성
    MD-->>README: 인용문 적용

    사용자->>MD: 코드 블록 작성
    MD-->>README: 코드 블록 적용

    Note over 사용자,Emoji: 3. README.md에 이모지 활용

    사용자->>Emoji: 이모지 선택
    Emoji-->>사용자: 사용할 이모지 제공

    사용자->>README: 이모지 직접 입력
    사용자->>README: 이모지 단축코드 사용
    사용자->>README: 운영체제 단축키로 이모지 입력

    README-->>사용자: 시각적으로 구분된 문서 완성

    Note over 사용자,README: 4. 이모지를 활용한 README 구성

    사용자->>README: 섹션 제목에 이모지 추가
    사용자->>README: 주요 기능에 이모지 추가
    사용자->>README: 설치 과정에 이모지 추가
    사용자->>README: 문서 및 안내 영역에 이모지 추가

    README-->>사용자: 가독성 높은 README.md 완성

    Note over 사용자,GitHub: 5. GitHub에서 README.md 활용

    사용자->>GitHub: README.md 저장소에 업로드
    GitHub->>README: README.md 내용 읽기
    README-->>GitHub: Markdown 문서 구조 전달
    GitHub->>GitHub: Markdown 렌더링
    GitHub->>GitHub: 이모지 렌더링
    GitHub-->>사용자: 완성된 README.md 화면 표시

    Note over 사용자,GitHub: Markdown과 이모지를 활용한 프로젝트 README 완성
    사용자->>GitHub: README.md 업로드
    GitHub-->>사용자: 프로젝트 문서 표시
