# ROS 2 Study · KPOL

SeSAC Physical AI 강남 3기 ROS2 스터디 (4명: Kang, Park, Oh, Lee)
매주 화·목 1시간 · Discord 온라인 · 2026-10-27 ~ 11/12

> 계획, 세션 캘린더, 📒 오답노트, 📖 매일 복습 기록은 **노션**에 있다. 이 레포는 **코드**만 모은다.

## 진행 방식

| 시간 | 내용 |
|---|---|
| 0–25분 | 핑크랩 PPT 강의자료로 수업 내용을 말로 설명 |
| 25–50분 | 모르는 부분 공유 · 함께 풀기 (필요하면 이 레포의 수업 코드를 같이 본다) |
| 50–60분 | 노션 오답노트 정리 |

## 폴더 구조

```
ros2-study-kpol/
├── class-code/            # 수업 코드 (Lee가 날짜별로 올림)
│   └── 2026-10-27_ros2-basics/
├── practice/              # 각자 "다시 짜기" 연습 코드
│   ├── kang/
│   ├── park/
│   ├── oh/
│   └── lee/
└── docs/
    └── daily-review.md    # 매일 복습 루틴
```

- **class-code/**: 수업 날짜와 주제로 폴더 이름을 짓는다. 예: `2026-10-28_topic-pubsub`
- **practice/<이름>/**: 수업 코드를 보지 않고 다시 짠 코드. 틀려도 괜찮다. 막혔던 부분은 노션 오답노트로.

## 수업 코드 실행하기

ROS2 패키지는 colcon 워크스페이스의 `src/` 안에 있어야 빌드된다. 레포를 클론한 뒤 실행하고 싶은 패키지를 워크스페이스로 링크한다.

```bash
git clone https://github.com/glorybell1984/ros2-study-kpol.git ~/ros2-study-kpol

mkdir -p ~/ros2_ws/src
ln -s ~/ros2-study-kpol/class-code/2026-10-28_topic-pubsub/<패키지> ~/ros2_ws/src/

cd ~/ros2_ws
colcon build --symlink-install
source install/setup.bash
```

## 올리는 규칙

1. 자기 폴더(`practice/<이름>/`)는 main에 바로 push해도 된다.
2. `class-code/`와 README 수정은 Lee가 관리한다. 고칠 게 있으면 노션이나 Discord로 알려 주기.
3. `build/`, `install/`, `log/`는 올리지 않는다 (`.gitignore`에 들어 있음).
