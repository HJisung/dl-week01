# 🚀 개인 지식 관리 시스템 (PKMS) 구축 계획

본 프로젝트는 전공 지식(CS), 최신 기술 실습(Tech), 트러블슈팅(Blog), 개인 기록(Log)을 체계적으로 분리하여 관리하는 것을 목표로 함.

---

## 🏗️ 4단계 지식 관리 아키텍처

| 계층        | 프로젝트명         | 성격           | 주요 콘텐츠                                     | 권장 기술 스택                                   |
| :---------- | :----------------- | :------------- | :---------------------------------------------- | :----------------------------------------------- |
| **Layer 1** | **CS & Math Docs** | 정적 (Static)  | 운영체제, 네트워크, 자료구조, 수학 등 기초 지식 | Next.js, Nextra, Markdown                        |
| **Layer 2** | **Tech Playbook**  | 동적 (Dynamic) | Next.js, Apollo Client, TSX 실습 예제 및 문서   | Next.js (App Router), MDX, Contentlayer          |
| **Layer 3** | **Tech Blog**      | 기록 (Log)     | 문제 해결(Troubleshooting), 회고, 기술 통찰     | Next.js, Tailwind CSS, Shiki (Code Highlighting) |
| **Layer 4** | **Life Log/Diary** | 개인 (Private) | 15분 단위 한 줄 로그, 일기, 루틴 관리           | Next.js, Supabase(DB), Git-flow UI               |

---

## 📂 프로젝트별 상세 설계

### 1. CS & Math Docs (뿌리 지식)

- **목표:** 시간이 지나도 변하지 않는 근본 원리를 나만의 언어로 정리.
- **특징:** 검색 최적화 및 계층 구조 중심.
- **핵심:** 복학 대비 전공 필수 과목 위주로 구성.

### 2. Tech Playbook (기술 실험실)

- **목표:** 공식 문서를 따라 하는 수준을 넘어, 직접 코드를 실행하며 배우는 실습장.
- **특징:** 마크다운 내부에 실제 TSX 컴포넌트(Apollo Client 등)를 삽입하여 동작 확인. (mdx + tsx)
- **기술 포인트:** `rehype-pretty-code`를 통한 코드 줄 강조, `Contentlayer`를 통한 타입 안전성 확보.

### 3. Tech Blog (성장 기록)

- **목표:** 공부하며 겪은 시행착오와 깨달음을 외부와 공유 가능한 형태로 기록.
- **특징:** "왜 이 기술을 썼는가?"와 "어떻게 해결했는가?"에 집중.
- **연결:** Docs나 Playbook의 특정 개념을 링크로 연결하여 지식의 그물망 형성.

### 4. Life Log & Diary (메타인지)

- **목표:** 15-30분 단위의 활동 로그를 통한 시간 관리 및 감정 기록.
- **특징:** Git-flow 스타일의 UI(Commit = 완료, Merge = 하루 마감) 적용.
- **기능:** 빠른 입력을 위한 간결한 인터페이스 및 개인적인 회고.

---

## 🛠️ 공통 기술 가이드라인

1. **Type Safety:** 모든 프로젝트는 TypeScript를 기본으로 하여 데이터 구조와 props 타입을 엄격히 관리함.
2. **Component Reuse:** Playbook에서 검증된 컴포넌트는 실제 서비스나 블로그 UI에 재활용함.
3. **Automated Workflow:** 가능하면 Vercel 등을 통해 자동 배포 환경을 구축하여 기록의 연속성을 유지함.

---

## 📅 향후 로드맵

1. **[진행중]** Layer 1: Nextra 기반 CS Docs 기본 틀 구축 및 운영체제 정리 시작.
2. **[예정]** Layer 2: Next.js + MDX 환경 설정 및 Apollo Client 실습 페이지 구현.
3. **[예정]** Layer 4: Git-flow UI 다이어리 설계 및 DB 연동.
4. **[예정]** Layer 3: 블로그 디자인 및 콘텐츠 마이그레이션.
