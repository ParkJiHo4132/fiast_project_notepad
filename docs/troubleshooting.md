# 메모장 앱 — 트러블슈팅 기록

---

## 2026-06-06

### 문제: GitHub 레포지토리 이름에 dash(-) 사용 시 Flutter 프로젝트 생성 불가

**상황**
GitHub에서 레포지토리 이름을 `fiast-project-notepad`처럼 dash(`-`)를 포함해 생성한 뒤, 해당 이름으로 Flutter 프로젝트를 구성하려 했으나 오류 발생.

**원인**
Flutter 패키지명(`pubspec.yaml`의 `name` 필드)은 Dart 식별자 규칙을 따르기 때문에 dash(`-`)를 사용할 수 없고, 소문자와 underscore(`_`)만 허용됨.

**해결**
GitHub 레포지토리 이름을 `fiast_project_notepad`(dash → underscore)로 수정 후 다시 클론하여 프로젝트 재구성.

**교훈**
Flutter/Dart 프로젝트는 처음부터 레포 이름을 `snake_case`로 만들 것.

---
