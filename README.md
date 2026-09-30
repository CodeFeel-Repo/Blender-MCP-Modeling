# ROK-Weapon-Release

K2 Black Panther(흑표)의 Blender 작업 파일, 외형 모델링용 참고 도안 및 AI 작업 지침을 보관하는 저장소입니다. 게임·영상·전시용 비기능성 3D 외형 모델링을 목적으로 합니다.

## 포함 파일

| 파일 | 설명 |
| --- | --- |
| [K2 - Black Panther.blend](K2%20-%20Black%20Panther/K2%20-%20Black%20Panther.blend) | K2 Black Panther Blender 프로젝트 |
| [K2 도안 폴더](K2%20-%20Black%20Panther/) | 정투영 이미지 5장과 사선 참고 이미지 4장 |
| [01.Design.md](01.Design.md) | 참고 이미지와 입력 치수를 바탕으로 단일 방향 도안을 제작하는 작업 지침 |
| [02.Modeling.md](02.Modeling.md) | 도안을 분석하여 Blender MCP로 새 외형 모델을 만드는 작업 지침 |

## 사용 환경

- **Blender**: `.blend` 작업 파일을 열고 편집할 때 사용합니다.
- **Git**: 아래 명령으로 저장소를 내려받을 때 사용합니다. ZIP 다운로드도 가능합니다.
- **Blender MCP가 연결된 AI 환경**: `02.Modeling.md`를 이용한 새 모델링 작업에 필요합니다.

## 시작하기

1. 저장소를 복제합니다.

   ```sh
   git clone https://github.com/CodeFeel-Repo/Blender-MCP-Modeling.git ROK-Weapon-Release
   ```

   Git을 사용하지 않는 경우 저장소의 **Code → Download ZIP**으로 내려받은 뒤 압축을 풉니다.

2. Blender를 실행하고 **File → Open**에서 `K2 - Black Panther/K2 - Black Panther.blend`를 엽니다.
3. 모델을 확인하거나 편집합니다. 원본을 보관하려면 **File → Save As**로 다른 이름으로 저장합니다.

## 저장소 구조

```text
ROK-Weapon-Release/
├── README.md
├── 01.Design.md
├── 02.Modeling.md
└── K2 - Black Panther/
    ├── K2 - Black Panther.blend
    ├── FRONT.png
    ├── REAR.png
    ├── LEFT.png
    ├── RIGHT.png
    ├── TOP.png
    ├── FRONT_LEFT_THREE_QUARTER.png
    ├── FRONT_RIGHT_THREE_QUARTER.png
    ├── REAR_LEFT_THREE_QUARTER.png
    └── REAR_RIGHT_THREE_QUARTER.png
```

## 도안 제작 및 새 모델링

두 Markdown 문서는 AI 도구에 전달할 작업 지침입니다. 기존 모델을 열어 확인하는 경우에는 별도로 실행할 필요가 없습니다.

1. **도안 제작:** `01.Design.md`의 사용자 입력에 대상 이름, 참고 이미지, 기준 상태, 실제 치수 및 출력 방향을 채웁니다. 방향별로 하나의 도안을 제작하고 동일한 단위와 스케일 기준을 유지합니다.
2. **도안 준비:** 생성한 도안을 대상별 작업 폴더에 모읍니다. K2 폴더에는 전후좌우·상단 정투영 이미지와 네 방향의 사선 이미지가 있습니다.
3. **새 모델링:** Blender MCP가 연결된 환경에서 `02.Modeling.md`와 작업 폴더를 지정합니다. 이 지침은 현재 Scene의 모든 객체를 삭제하고 새 모델을 만드는 절차이므로, 실행 전에 진행 중인 작업을 저장합니다.
4. **검증 및 저장:** 도안에서 확인한 치수·방향과 모델을 비교하고, 참고 이미지 보존 및 Pack 여부를 확인한 뒤 새로운 파일명으로 저장합니다. 확인할 수 없는 치수나 형태는 추측하지 않고 결과에 기록합니다.

상세한 분석·모델링·검증 기준은 각 작업 지침을 참고하세요. 도안은 실제 대상의 제작·가공용 도면이 아닙니다.

## 좌표 및 단위 기준

작업 지침에서 사용하는 모델 좌표계는 다음과 같습니다.

| 축 | 방향 |
| --- | --- |
| +X / -X | 오른쪽 / 왼쪽 |
| +Y / -Y | 후방 / 전방 |
| +Z / -Z | 위 / 아래 |

좌우 중앙 대칭면은 `X = 0`입니다. 도안 제작 지침의 기본 단위는 **Metric**, **Unit Scale 1.0**, **1 BU = 1 m**입니다. 대상별 치수와 도안의 방향 표기를 확인하여 작업 기준을 결정합니다.
