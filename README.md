# 2026-git-start

로컬에서 추가한 내용입니다!
github 웹에서 추가한 내용입니다


오늘의 학습 목표: 작업자 B의 Merge 충돌 실습

오늘의 학습 목표: Git 협업 이해
오늘의 학습 목표: 작업자 A의 Git 협업 실습

# Git 협업 실습 Sequence Diagram

## 1단계. 충돌 없는 협업

```mermaid
sequenceDiagram
    actor A as 작업자 A
    participant GitHub as GitHub origin/main
    actor B as 작업자 B

    A->>A: worker-a.md 생성
    A->>A: git add worker-a.md
    A->>A: git commit -m "A: 작업자 A 문서 추가"
    A->>GitHub: git push

    B->>GitHub: git fetch origin
    GitHub-->>B: origin/main 갱신
    B->>B: git log --oneline main..origin/main
    B->>B: git merge origin/main

    B->>B: worker-b.md 생성
    B->>B: git add worker-b.md
    B->>B: git commit -m "B: 작업자 B 문서 추가"
    B->>GitHub: git push

    A->>GitHub: git fetch origin
    GitHub-->>A: origin/main 갱신
    A->>A: git log --oneline main..origin/main
    A->>A: git merge origin/main
```

## 2단계. Merge 충돌 및 해결

```mermaid
sequenceDiagram
    actor A as 작업자 A
    participant GitHub as GitHub origin/main
    actor B as 작업자 B

    A->>A: README.md 수정
    A->>A: git add README.md
    A->>A: git commit -m "A: README 학습 목표 수정"
    A->>GitHub: git push

    B->>B: README.md 같은 문장 수정
    B->>B: git add README.md
    B->>B: git commit -m "B: README 학습 목표 수정"
    B->>GitHub: git push
    GitHub-->>B: rejected - fetch first

    B->>GitHub: git fetch origin
    GitHub-->>B: origin/main 갱신
    B->>B: git log --oneline --graph --all --decorate
    B->>B: git merge origin/main
    Note over B: README.md CONFLICT

    B->>B: README.md 충돌 내용 수정
    B->>B: git add README.md
    B->>B: git commit -m "B: A의 변경과 README 충돌 해결"
    B->>GitHub: git push

    A->>GitHub: git fetch origin
    GitHub-->>A: origin/main 갱신
    A->>A: git log --oneline main..origin/main
    A->>A: git merge origin/main
    A->>A: cat README.md
```
