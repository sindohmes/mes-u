[Eng](manual_mdm.md) / 한글

## 1. Start

Start는 시작 공정을 나타냅니다. 특정 작업 오더(이하 Job)에서 생성된 일련번호를 바탕으로 생성된 스캔용 바코드를 입력하면 시작공정을 진행한 것으로 입력됩니다. 실적이 입력된 후에는 금일 사용자가 입력한 시작 공정의 이력도 같이 실시간으로 조회됩니다.

![Start](./images/s301.png)

## 2. Input Parts
Input Parts는 부품 투입 공정을 나타냅니다. 

특정 작업 오더(이하 Job)에서 생성된 일련번호를 바탕으로 생성된 스캔용 바코드를 입력하면, 초기 입력 시에는 입력된 일련번호에 해당되는 투입 공정 목록을 조회하며, 특정 공정을 선택할 경우에 해당 공정의 목록이 화면에 조회됩니다.

공정 목록이 조회된 후에 스캔용 바코드를 다시 재 입력하면, 투입 부품에 대한 바코드를 입력할 수 있는 칸을 제공하며, 해당되는 내역을 입력하면 완성 제품에 어떤 부품을 투입하는 지에 대한 이력이 입력됩니다. 실적이 입력된 후에는 금일 사용자가 입력한 부품 투입 공정의 이력도 같이 실시간으로 조회됩니다.

투입 공정 목록이 설정될 경우, 같은 오더 또는 같은 품번을 가진 스캔용 바코드를 입력하면 투입 공정 목록을 조회할 필요 없이 즉시 부품 투입을 위한 항목으로 이동되지만 다른 품번을 가진 스캔용 바코드를 입력하면 다시 재설정을 해야 하는 점도 참고 바랍니다.

![Input Parts](./images/s302.png)


## 3. Completion
Comletion은 Job에서 생성된 일련번호에 대한 생산이 완료되었을 때 생산품에 대한 스캔용 바코드를 입력하면 완성공정을 진행한 것으로 입력됩니다. 이 부분은 실적과도 연결된 부분이기 때문에 외부 ERP를 사용할 경우 연동하는 기능을 개발하는 것을 권장하며, 완성공정에 연동된 출력물이 있을 경우에는 출력물도 동시에 나올 수 있는 기능을 제공합니다.

![Completion](./images/s303.png)

## 4. Inline inspection

Inspection은 Job 공정 내 검사를 수행할 때 검사를 위한 스캔용 바코드를 입력하면, 일련번호에 해당되는 검사 공정 목록을 조회하며, 검사 결과를 입력할 수 있는 화면을 제공합니다. 검사 결과는 현재 PASS/FAIL만 입력 가능하지만, 다음 버전에서는 수치 및 여러 가지 값을 입력해서 나타낼 수 있도록 개선할 예정입니다.

일반적으로 검사는 납입 검사, 공정 내 검사, 출하 검사 등이 있지만, 납입 검사 및 출하 검사는 아직 구현되지 않은 관계로 추후 부품 입고 및 출하 기능을 구현할 경우 동시에 구현할 예정이며, 현재는 공정 내 검사만 이용 가능한 점 참고 바랍니다.

![Inspection](./images/s304.png)


## 5. Inline Repair

Repair는 공정 내 검사에서 불량(FAIL)이 발생한 일련번호에 대해서 수리를 진행할 경우, 수리에 대한 세부 내용을 입력합니다. 불량 및 수리는 불량 코드 기준정보를 바탕으로 해서 불량 내역 및 수리 내역을 입력할 수 있으며, 대체 부품이 있을 경우 대체 부품에 대한 스캔용 바코드를 입력하는 기능도 같이 제공합니다.

![Repair](./images/s305.png)

## 6. Packing

Packing은 이미 제조가 완성된 일련번호를 대상으로 포장을 진행하는 공정입니다. 포장 공정은 일반적으로 Pallet, Box 를 단위로 포장을 진행하나, 추가 단위 및 관리 부분은 다음 버전에서 개선할 예정이며, 포장 번호를 입력하지 않고 제품의 일련번호만 입력할 경우에는 포장 번호가 자동으로 생성됩니다. 반면 포장번호를 입력할 경우에는 해당 번호에 맞게 포장이 이루어집니다.

포장 단위는 품목 별로 설정되어 있으며, 포장 개수를 모두 충족할 경우에는 자동으로 포장이 완료된 것으로 입력되며, 포장을 중간에 완료할 경우에도 포장할 수 있는 기능도 제공하고 있습니다.

또한 포장 공정에 연결된 출력물이 있을 경우에는 출력물을 출력할 수 있는 기능도 동시에 제공합니다.

![Packing](./images/s306.png)


## 7. Executable Systems

Executable Systems는 생산 공정 내 외부 프로그램을 사용할 때 수행되는 화면으로, 현재는 Internet Explorer 10.0 이상 버전에서만 지원됩니다. 웹 애플리케이션 특성 상 해당 기능은 추후 개선 시 제외될 수도 있으며, 이와 관련해서는 사용자들의 피드백을 통해서 결정하겠습니다.

![Executable Systems](./images/s307.png)

## 8. Assembly Monitoring

Assembly Monitoring은 공정 내 이루어진 모든 이력을 조회할 수 있는 화면으로, 다양한 검색 조건을 바탕으로 검색 결과를 제공합니다.

![Assembly Monitoring](./images/s308.png)


<div style="text-align:right">
    <p><a href='./manual_system_mgmt.ko-KR.md'>→ System Management</a></p>
    <p><a href='./manual_mdm.ko-KR.md'>→ Master Data Management</a></p>
    <p><a href='./manual_production_mgmt.ko-KR.md'>→ Production Management</a></p>
</div>