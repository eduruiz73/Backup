---

copyright:
  years: 2014, 2018
lastupdated: "2018-06-05"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# 開始使用 EVault 備份服務

備份可確保您的資料是在裝置之外安全地儲存，而且在遺失時受到保護。EVault 備份是一種透過 EVault WebCC 瀏覽器型管理公用程式來管理的自動化代理程式型備份系統，提供使用者在「{{site.data.keyword.BluSoftlayer_full}}網路」的一個以上資料中心內伺服器之間備份資料的方法。管理者可以設定備份來遵循每小時、每日、每週或自訂排程，將完整系統、特定目錄或甚至個別檔案設成目標。其他外掛程式容許與 Microsoft Exchange 和 Microsoft SQL 之類的軟體，以及其他類型的協力廠商軟體相容，並在必要時可讓使用者執行「裸機還原」。

## 訂購 EVault 

購買 EVault 備份服務的方式有兩種：

- 訂購伺服器時購買 EVault
- 以升級方式購買 EVault

### 訂購伺服器時購買 EVault

1. 登入 [IBM Cloud 型錄](https://console.bluemix.net/catalog/){:new_window}或 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}。
2. 訂購每月裸機伺服器。您可以在[這裡](https://console.bluemix.net/docs/bare-metal/baremetal-provision.html){:new_window}進一步瞭解如何訂購裸機伺服器。
3. 系統會將您重新導向至管理入口網站，以完成訂單。<br/>
  **附註**：訂購每小時計費伺服器時，無法使用 EVault 備份服務。不過，稍後可用升級方式新增此服務。 
4. 在**附加程式**區段下，選擇其中一個 EVault 選項（「無」以外）。
6. 在頁面底端，按一下**新增至訂單**。即會顯示「移出」頁面。
7. 在**移出**頁面上，尋找「主機及網域名稱」 區段，並輸入主機及網域名稱。您可以選擇您喜歡的任何主機名稱及「網域」。
8. 在**移出**頁面的右側，按一下**雲端服務條款**和**協力廠商服務合約**勾選框。
9. 確認或輸入您的付款資訊，然後按一下**提交訂單**。系統會將您重新導向至具有佈建訂單號碼的畫面。您可以列印此畫面，因為它也是您的佈建訂單收據。<br/>**附註**：您也可以按一下**儲存為報價**來儲存此訂單，而不購買。

一系列電子郵件會傳送給您的管理者：確認佈建訂單、佈建訂單核准和處理，以及佈建完成。在您登入 {{site.data.keyword.cloud_notm}} 之後，佈建完成電子郵件會包含*裝置詳細資料*頁面的鏈結。您也可以直接登入 {{site.data.keyword.slportal}}。

**確認 EVault 服務購買**
1. 在 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} 中，從主功能表中選取**裝置** > **裝置清單**。 
2. 找出您已訂購的新伺服器。
  - 如果 URL 旁邊有時鐘圖示，則您將需要等待，以繼續進行 EVault 購買確認。您可以重新整理頁面，以在新伺服器上查看已更新的狀態。當時鐘圖示不再呈現時，您可以繼續進行接下來的步驟，以確認 EVault 服務購買。
  - 當您的伺服器不再顯示時鐘圖示時，請按一下鏈結（伺服器的 URL），移至**裝置詳細資料**頁面。 
3. 按一下**儲存空間**標籤，以顯示 EVault 資訊。
4. 檢查 EVault 區段，並驗證 EVault 採購程序期間所選取的大小是否顯示在 EVault 鏈結旁邊。

### 以升級方式購買 EVault

**選取要安裝 EVault 的伺服器**
1. 登入 [IBM Cloud 型錄](https://console.bluemix.net/catalog/){:new_window}或 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}。
2. 從主功能表中選取**裝置** > **裝置清單**。尋找您要為其新增 EVault 服務的裝置。
3. 按一下「裝置」名稱，以移至「裝置詳細資料」頁面。

**新增（購買）EVault 服務**
1. 按一下**儲存空間**標籤，然後找出靠近頁面底端的 Evault 區段。
2. 按一下**新增**鏈結。
3. 在蹦現畫面中，選取一個位置或接受預設值，並選取大小。
4. 按一下**繼續**。
5. 如果您同意條款，請按一下勾選框。
6. 按一下**下訂單**。

**確認 EVault 服務購買**
1. 重新整理**裝置詳細資料**頁面，並確保已選取**儲存空間**標籤。
2. 檢查 EVault 區段，並驗證 EVault 採購程序期間所選取的大小是否顯示在 EVault 鏈結旁邊。<br /> **附註**：如果 EVault 儲存空間大小繼續顯示零容量，則可能需要重新整理第二頁。 

## 存取及檢視 {{site.data.keyword.slportal}} 中的 EVault 備份儲存空間詳細資料

您可以隨時使用 {{site.data.keyword.slportal}} 來檢視有關 EVault 備份服務的儲存空間詳細資料。可能檢視的詳細資料包括與所選取 EVault 備份服務相關聯的密碼、儲存空間位址及使用情形。 

1. 若要存取 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} 中的 **EVault 備份儲存空間**畫面，請使用您的唯一認證登入。
2. 按一下**儲存空間**，然後從下拉清單中選取**備份**。
2. 按一下列上的任何位置，以取得所需「EVault 備份」來檢視其儲存空間詳細資料。從這個視圖中，看不到密碼。繼續進行下一步，以檢視與「EVault 備份」服務相關聯的密碼。
3. 按一下**密碼**欄位旁邊的**顯示**勾選框，以檢視所選取「EVault 備份」服務的密碼。

對於許多 {{site.data.keyword.BluSoftlayer_full}} 產品及服務，{{site.data.keyword.slportal}} 內的密碼儲存空間功能僅用於儲存或追蹤密碼，而對 {{site.data.keyword.slportal}} 內的密碼所做的變更不會套用至產品或服務。這與「EVault 備份」_無關_。對 {{site.data.keyword.slportal}} 內「EVault 備份」密碼所做的變更將是針對服務本身所做的。進行變更時，請謹記它們將直接影響您的服務。若要重設密碼，請遵循[如何在 {{site.data.keyword.slportal}} 變更 EVault 備份密碼](/docs/infrastructure/Backup/change-password-evault-backup-service.html)中的步驟。

## 安裝 EVault 代理程式

下列作業系統支援「EVault 代理程式」：

### Windows
 - Windows Server 2012 R2
 - Windows Server 2012
 - Windows Server 2008 R2
 - Windows Server 2008

### Linux
 - CentOS 7.x
 - CentOS 6.x
 - Debian GNU/Linux 9.x
 - Debian GNU/Linux 8.x
 - Debian GNU/Linux 7.x
 - Red Hat Enterprise Linux 7.x
 - Red Hat Enterprise Linux 6.x
 - Ubuntu Linux 16.04
 - Ubuntu Linux 14.04

請遵循適合您作業系統的指示：
- [在 Linux 中安裝 EVault 備份用戶端](install-evault-backup-client-linux.html)
- [在 Windows 中安裝 EVault 備份用戶端](install-evault-backup-client-windows.html)
- [安裝 EVault Backup Client for Windows 2016](install-evault-windows2016.html)

## 存取 WebCentralControl (WebCC) for EVault Backup

WebCentralControl (WebCC) 是與 {{site.data.keyword.BluSoftlayer_full}} 所提供之任何「EVault 備份」服務互動時所使用的用戶端。WebCC 是瀏覽器型用戶端，可在我們的專用網路上執行，容許完全控制任何「EVault 備份」服務，包括配置及還原。請遵循下列步驟來存取 WebCC for EVault Backup。

1. 透過 VPN 存取「專用網路」。<br/>
    **附註**：無法透過公用網路存取 WebCC。必須建立 VPN 連線才能存取 WebCC。
2. 存取 [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} 中的「EVault 備份儲存空間」畫面。
3. 按一下列上的任何位置，以取得所需「EVault 備份」來展開視圖。
3. 按一下 **WebCC 登入**，在瀏覽器中啟動 WebCC 用戶端。

## 在 WebCC 中配置 EVault 代理程式

一旦您訂購了 EVault 服務，並在伺服器上安裝了代理程式，就可以開始建立資料備份。請遵循下列步驟來配置代理程式、配置保留排程，以及啟動第一個備份工作。

1. 登入 WebCc。
2. 按一下**所有代理程式** > **未配置的代理程式**。
3. 按一下**這是我想要配置的新代理程式**鏈結。逐步執行處理程序，並指定下列各項：
   1. 代理程式配置 - 提供代理程式說明，並按**下一步**。
   2. 工作類型選項 - 輸入工作名稱、工作說明和備份來源類型，並按**下一步**。
   3. 選項 - 選取目錄並按一下**併入...**。
   4. 選項 - 提供密碼
   5. 排程 - 按一下**新增**以建立排程，並按**下一步**。
   6. 選取預設儲存庫，並按一下**確定**。
   7. 按一下**儲存**。
4. 建立保留排程：
   1. 選取**編輯** > **代理程式設定**。
   2. 按一下**新增**。
   3. 填寫您的保留詳細資料。
   4. 按一下**確定**。
   5. 按一下**儲存**。
   **附註** - 在[這裡](evault-backup-faq.html#how-do-the-retention-schemes-work-)進一步閱讀「保留方案」的運作方式。
5. 執行代理程式並啟動備份。
   1. 按一下**所有代理程式**，然後選取您剛才配置的代理程式。
   2. 按一下**執行備份**。
   3. 確認「目的地」，並選取保留方案。
   4. 按一下**啟動備份**。您可以在處理程序執行時檢視備份詳細資料。
   5. 當備份完成時，請按一下**關閉**。
   
**附註**：在[這裡](configure-simple-file-backup-linux.html)進一步閱讀如何在 Linux 上配置簡單的檔案層次備份。

## 接下來會發生什麼情況

WebCC 的系統有完整的文件說明，並支援可在 WebCC 內存取應用程式。按一下右上角的**說明**，以藍色圓圈中的白色問號表示。按一下蹦現方框左側導覽列中的任何文章或主題，以檢視相關資訊。

