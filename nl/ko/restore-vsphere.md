---

copyright:
  years: 1994, 2019
lastupdated: "2019-03-29"

keywords: IBM Cloud Backup, VMware, VRA, vSphere Recovery Agent, plug-in, plugin, EVault, Carbonite, vSphere

subcollection: Backup

---
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:DomainName: data-hd-keyref="APPDomain"}
{:DomainName: data-hd-keyref="DomainName"}

# vSphere 데이터 복원
{: #VRARestore}
 
VM이 vSphere 환경에서 보호되는 경우, vSphere 복구 에이전트를 사용하여 [vSphere VM](#restoreVMs)을 복원하고 [파일 및 폴더를 복원](#restoreFFVRA)할 수 있습니다.

## vSphere VM 복원
{: #restoreVMs}

1.	탐색줄에서 **컴퓨터**를 클릭하십시오. 그리드에 사용 가능한 컴퓨터가 표시됩니다. 
2.	복원할 VM이 있는 vSphere 환경을 찾은 다음 행을 클릭하여 보기를 펼치십시오. 
3.	**작업**을 클릭하십시오. 
4.	복원할 VM이 있는 백업 작업을 찾은 다음 작업의 **조치 선택** 메뉴에서 **복원**을 클릭하십시오. 
5.	**복원할 대상 선택** 대화 상자에서 **가상 머신**을 선택하십시오. 
6.	**계속**을 클릭하십시오. 복원 대화 상자에 작업에 대한 최신 safe-set가 표시됩니다. 
    * 다른 소스에서 데이터를 복원하려면 **소스 디바이스** 목록에서 소스(저장소)를 클릭하십시오. 
    *	이전 safe-set에서 복원하려면 **safe-set 찾아보기** 단추를 클릭하십시오. 표시되는 달력에서 복원할 safe-set의 날짜를 클릭하십시오. 
7.	**복원할 항목** 패널에서 복원할 각 VM을 선택하십시오. 
8.	**암호화 비밀번호** 필드에 데이터 암호화 비밀번호를 입력하십시오. 
9.	**대상 데이터 저장소** 목록에서 복원된 VM의 데이터 저장소를 클릭하십시오. 
10.	VM을 사용자가 선택한 데이터 저장소로 복원하려면 다음 옵션 중 하나를 선택하십시오.
  * **선택된 모든 가상 머신을 선택된 데이터 저장소로만 복원합니다.**
  * **가상 머신의 원래 데이터 저장소를 사용할 수 없는 경우에만 선택된 데이터 저장소로 복원합니다.** 백업된 VM에 두 개 이상의 데이터 저장소에 상주하는 다중 VMDK가 포함되어 있으며 데이터 저장소 중 하나 이상이 사용 불가능한 경우, 전체 VM이 선택된 데이터 저장소로 복원됩니다. 

  VM 또는 템플리트를 vCenter로 복원하며 원래 VM이 있는 경우, VM이 다음 이름을 사용하여 원래 VM의 복제본으로 복원됩니다. <VMname>-vra-restored-<Date>. 원래 VM의 전원이 켜져 있거나 꺼져 있거나 일시중단된 경우, VM이 복제본으로 복원됩니다. 원래 VM의 전원이 켜져 있고 정적 IP 주소를 사용하는 경우, 복제된 VM의 전원이 켜져 있으면 복원될 때 IP 주소 충돌이 발생할 수 있습니다.
  {:note}

13.	**대상 호스트** 목록에서 VM을 등록할 호스트를 클릭하십시오. 목록에는 선택된 데이터 저장소에 대한 액세스 권한이 있는 호스트만 표시됩니다.
14.	복원된 VM을 사용자가 선택한 호스트에 등록하려면 다음 옵션 중 하나를 선택하십시오. 
  * **선택된 모든 가상 머신을 선택된 호스트에만 등록합니다.**
  * **가상 머신의 원래 호스트를 사용할 수 없는 경우에만 선택된 호스트에 등록합니다.** 
15.	VM이 복원된 후에 전원을 공급하려면 **복원 후에 VM 전원 공급**을 선택하십시오. 
16.	**성능 옵션**에서 기본 설정을 유지하십시오. 
17.	**복원 실행**을 클릭하십시오.

## 파일 및 폴더 복원
{: #restoreFFVRA}

VRA(vSphere Recovery Agent)를 사용하여 보호되는 Windows VM에서 파일 및 폴더를 복원할 수 있습니다. 동시에 둘 이상의 VM에서 파일 및 폴더를 복원할 수 있습니다. VRA를 사용하여 Linux VM에서 파일 및 폴더를 복원할 수는 없습니다.
{:important}

파일 및 폴더 복원 동안 선택된 VM의 볼륨이 VRA가 실행 중인 머신에 드라이브로 마운트됩니다. 그런 다음 사용자가 드라이브에서 파일 및 폴더를 복사할 수 있도록 마운트된 드라이브의 일부 또는 전부를 공유할 수 있습니다. 또한 VRA 머신에 로그인하여 마운트된 드라이브에서 파일 및 폴더를 복사할 수 있습니다. 

디스크의 파일 및 폴더는 비관리자를 포함하여 VRA 시스템의 누구나 액세스 가능합니다. 보안이 걱정되면 에이전트 시스템에 보안을 제공하고 사용자가 로컬로 머신에 로그인하는 것을 방지하십시오.
{:tip}

1. 탐색줄에서 **컴퓨터**를 클릭하십시오. 그리드에 사용 가능한 컴퓨터가 표시됩니다.
2. 복원할 VM이 있는 vSphere 환경을 찾은 다음 행을 클릭하여 보기를 펼치십시오.
3. **작업**을 클릭하십시오. 
4. 복원할 VM이 있는 백업 작업을 찾은 다음 작업의 **조치 선택** 메뉴에서 **복원**을 클릭하십시오.
5. **복원할 대상 선택** 대화 상자에서 **파일 및 폴더**를 선택하십시오.
6. **계속**을 클릭하십시오. 복원 대화 상자에 작업에 대한 최신 safe-set가 표시됩니다. 
  * 다른 리소스에서 데이터를 복원하려면 소스 디바이스 목록(저장소)에서 소스를 클릭하십시오.
  * 이전 safe-set에서 복원하려면 safe-set 찾아보기 단추를 클릭하십시오. 표시되는 달력에서 복원할 safe-set의 날짜를 클릭하십시오. 달력의 오른쪽에서 복원할 특정 safe-set를 클릭하십시오. 
7. **복원할 항목** 패널에서 복원할 파일 또는 폴더가 있는 VM을 선택하십시오. 
8. **암호화 비밀번호** 필드에 데이터 암호화 비밀번호를 입력하십시오. 
9. **유휴 시간 필드**에 공유 드라이브가 자동으로 비공유되기 전에 허용되는 비활성 분 수를 입력하십시오. 유휴 시간 범위는 2 - 180분입니다. 
    
    새 데이터가 복사되는 한 드라이브가 공유되지 않습니다. 둘 이상의 공유되는 드라이브에서 동일한 데이터를 복사하는 경우, 새 데이터를 읽을 수 없으므로 시스템이 제한시간을 초과할 수 있습니다.
    {:note}
    
10.	**성능 옵션**에서 사용 가능한 모든 대역폭 사용을 선택하십시오. 
11.	**복원 실행**을 클릭하십시오. 
12. 선택된 VM의 복원된 볼륨이 VRA가 실행 중인 머신에 드라이브로 맵핑되며 복원 마운트 폴더에서 사용 가능합니다. 다음 단계 중 하나를 수행하십시오.
  * 맵핑된 드라이브에서 복원할 파일 및 폴더를 복사하십시오. 
  * 하나 이상의 맵핑된 드라이브를 기타 사용자와 공유하십시오. 그런 다음 사용자가 UNC 공유에 액세스하여 복원할 파일 및 폴더를 복사할 수 있습니다. 
  * VRA 머신의 복원 마운트 폴더에서 하나 이상의 디렉토리를 공유하십시오. 그런 다음 사용자가 UNC 공유에 액세스하여 복원할 파일 및 폴더를 복사할 수 있습니다. 