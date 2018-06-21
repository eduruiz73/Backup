---

copyright:
  years: 1994, 2017
lastupdated: "2017-10-04"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# EVault 備份及還原術語 

## 差異技術：
第一個「備份」是「種子」（完整備份）、下一個及後續為差異備份（亦即，僅有變更），但它們相等於並仍可視為「完整備份」。亦即，您可以從其中還原所有或任何檔案。此技術容許在每個階段作業進行「完整備份」，但可節省「儲存庫」上的大量空間，並減少完成每個後續備份所需的時間量。

## 保留方案： 
EVault 容許「資料」保留，視您想要回復至多久以前而定。「每日保留」方案將保留資料 7 天、「每週」將保留資料 1 個月，而「每月」將保留資料 1 年。在每一個期間結束時，最舊的資料集會轉出，而第一個差異會變成最舊的可用還原點。 

## 壓縮： 
EVault 可對您的資料提供 6 種類型的加密解決方案：DES 56 位元、Blowfish 56 位元、三重 DES 演算法 112 位元、Blowfish 128 位元、AES 128 位元及 AES 256 位元。壓縮比例容許零壓縮至最大比例壓縮，根據檔案類型，在任何地方，此項壓縮可能從 20% 到 30%。

## 加密：
依預設，所有線上 (OTW) 加密都是利用 AES 128 位元加密來加密的。如果您想要以加密格式儲存資料，備份程序會有數個選項。請注意，如果您遺失密碼，就無法取回您的資料。 

## 特殊備份： 
系統狀態備份包括但不限於「COM + 類別登錄資料庫」、「登錄」、 「開機檔」、「系統檔案」、「效能計數器」，全部視您的「系統」而定。系統檔案會由於系統作業系統及服務套件而有所不同。通常它們有數千種之多。當您將這些 DLL 併入備份時，MS Windows 會建立這些 DLL 的動態清單。包括系統檔案可讓您從毀損的系統檔中回復，或如果您不小心解除安裝某些服務套件，或想要使用裸機還原進行回復，也可以進行回復。它可讓您回到備份的狀態，而不需要從安裝套件重新安裝作業系統，然後個別安裝每一個服務套件。 

## 開啟檔案： 
依預設，基本用戶端具有最先進的技術，可處理在作業系統上執行的大部分開啟檔案。在少數的情況下，如果備份由於開啟檔案限制而失敗，則有些次要外掛程式可供您買來改善開啟檔案的處理能力。經驗法則是您不需要開啟檔案外掛程式，除非在開啟檔案的備份中看到錯誤，在這種情況下您可以訂購這些外掛程式。