﻿---
title: '通訊清單: Exchange Online Help'
TOCTitle: 通訊清單
ms:assetid: 8ee2672a-3a45-4897-8cc0-fa23c374dbf9
ms:mtpsurl: https://technet.microsoft.com/zh-tw/library/Bb232119(v=EXCHG.150)
ms:contentKeyID: 50473715
ms.date: 04/24/2018
mtps_version: v=EXCHG.150
ms.translationtype: HT
---

# 通訊清單

 

_**適用版本：** Exchange Online, Exchange Server 2013_

_**上次修改主題的時間：** 2014-12-02_

*通訊清單*是收件者和其他 Active Directory 物件的集合。每份通訊清單都可包含一或多種物件 (例如，使用者、連絡人、群組、公用資料夾、會議室及設備資源)。您可以使用通訊清單來組織收件者及資源，以便輕鬆尋找您需要的收件者及資源。通訊清單會動態更新。因此，當新收件者新增至組織時，就會自動新增至適當的通訊清單。

如下圖所示，用戶端應用程式 (例如 Microsoft Outlook) 會顯示 Exchange 所提供的可用通訊清單。

**Microsoft Office Outlook 2007 中顯示的全域通訊清單**

![Outlook 2007 中顯示的通訊清單](images/Bb232119.54d7729c-2e28-4863-8944-b0c37dabbbb3(EXCHG.150).gif "Outlook 2007 中顯示的通訊清單")

通訊清單位在 Active Directory 中。因此，沒有連接至網路的行動使用者也就不會連接至這些伺服器端通訊清單。然而，您可以為沒有連接至網路的使用者建立離線通訊錄 (OAB)。這些 OAB 可下載至使用者的硬碟。通常若是要保存資源，OAB 是位於伺服器之實際通訊清單中的資訊子集。如需詳細資訊，請參閱 [離線通訊錄](offline-address-books-exchange-2013-help.md)。

**目錄**

預設通訊清單

自訂通訊清單

建立通訊清單的最佳作法

## 預設通訊清單

當使用者要使用其用戶端應用程式來尋找收件者資訊時，可以從可用的通訊清單中選取。有數種通訊清單會預設建立，例如全域通訊清單 (GAL)。Exchange 包含下列預設通訊清單，當有新的使用者、連絡人、群組或會議室新增至您的組織時，便會自動填入：

  - **所有連絡人**   此通訊清單包含組織中所有擁有郵件功能的連絡人。擁有郵件功能的連絡人就是具有外部電子郵件地址的收件者。如果您要讓組織中的所有使用者，都能使用擁有郵件功能的連絡人資訊，您必須將該連絡人加入 GAL 中。若要進一步了解郵件連絡人，請參閱[收件者](recipients-exchange-2013-help.md)。

  - **所有通訊群組清單**   此通訊清單包含擁有郵件功能的群組，例如組織中擁有郵件功能的安全性群組、通訊群組及動態通訊群組。擁有郵件功能的群組是為了加速寄送大量電子郵件及其他資訊而建立的收件者清單。將電子郵件傳送至擁有郵件功能的群組時，該清單中的所有成員都會收到該郵件的副本。若要進一步了解擁有郵件功能的群組，請參閱[收件者](recipients-exchange-2013-help.md)。

  - **所有會議室**   此通訊清單包含組織中被指派為會議室的所有資源。會議室是組織中的資源，可從用戶端應用程式傳送會議要求來進行排程。與會議室相關聯的使用者帳戶會停用。若要深入了解資源信箱的相關資訊，請參閱[收件者](recipients-exchange-2013-help.md)。

  - **所有使用者**   此通訊清單包含組織中所有擁有郵件功能的使用者。擁有郵件功能的使用者，代表 Exchange 組織之外的使用者。每個擁有郵件功能的使用者都有外部電子郵件地址。傳送給擁有郵件功能之使用者的所有郵件，都會路由傳送至這個外部電子郵件地址。擁有郵件功能的使用者與郵件連絡人相似，不同之處在於，擁有郵件功能的使用者具有 Active Directory 登入認證，並可存取資源。若要進一步了解擁有郵件功能的使用者，請參閱[收件者](recipients-exchange-2013-help.md)。

  - **預設全域通訊清單**   此通訊清單包含組織中擁有郵件功能的所有使用者、連絡人、群組或會議室。在設定期間，Exchange 會建立各種預設通訊清單。最熟悉的通訊清單是 GAL。依預設，GAL 包含 Exchange 組織中的所有收件者。換句話說，在已安裝 Active Directory 的 Exchange 樹系中，任何擁有信箱功能或郵件功能的物件都會列在 GAL 中。為方便使用，會依名稱而不是依電子郵件地址來組織 GAL。如需詳細資訊，請參閱 [建立全域通訊清單](create-a-global-address-list-exchange-2013-help.md)。

  - **公用資料夾**   此通訊清單包含組織中的所有公用資料夾。存取權限能判定誰可以檢視及使用這些資料夾。公用資料夾儲存於執行 Exchange 的電腦上。如需 Exchange 2013 中公用資料夾的相關資訊，請參閱[公用資料夾](public-folders-exchange-2013-help.md)。如需 Exchange Online 中公用資料夾的詳細資訊，請參閱 [Office 365 與 Exchange Online 的公用資料夾](https://technet.microsoft.com/zh-tw/library/jj200758\(v=exchg.150\))。

## 自訂通訊清單

Exchange 組織中可能包含數千個收件者。如果您將所有收件者編譯在預設通訊清單中，那些清單會變得相當大。為避免這種情況，您可以建立自訂通訊清單來協助組織中的使用者，以便他們尋找。

例如，假設一家公司有兩家大型子公司及一個 Exchange 組織。一個部門叫做 Fourth Coffee，負責進口及銷售咖啡豆。另一個部門 Contoso, Ltd 負責承購保險證。在每天大部分的活動中，Fourth Coffee 的員工並不會與 Contoso, Ltd 的員工通訊。因此，為方便員工尋找僅存在於其部門的收件者，您可以建立兩個新的自訂通訊清單，一個供 Fourth Coffee 使用，一個供 Contoso, Ltd 使用。在其部門搜尋收件者時，這些自訂通訊清單可讓員工只選取其部門專屬的通訊清單。然而，如果員工不確定收件者在哪個部門，就可以在 GAL 中搜尋，其中包含了兩個部門中的所有收件者。

您也可以建立通訊清單的子類別目錄，就叫做階層通訊清單。例如，您可以建立一個包含 Manchester 所有收件者的通訊清單，以及另一個包含 Stuttgart 所有收件者的通訊清單。

## 建立通訊清單的最佳作法

雖然通訊清單對使用者來說是很好用的工具，但是規劃不佳的通訊清單會讓人感到挫折。為確保使用者覺得您的通訊清單很實用，請考量下列最佳作法：

  - 避免建立太多通訊清單，使用者會不確定要在哪個清單中搜尋收件者。

  - 通訊錄清單應讓使用者更容易找到 GAL 中的地址。

  - 為通訊清單命名時，要讓使用者一眼就看出該清單包含哪些收件者類型。如果為您的通訊清單命名有困難，請不要建立太多清單，並提醒使用者他們可以使用 GAL 來尋找組織中的任何人。
    
    > [!NOTE]  
    > 根據 Exchange Online 的預設，「通訊清單」角色並未指派給任何角色群組。若要使用任何需要「通訊清單」角色的指令程式，您需將此角色新增至角色群組。如需詳細資訊，請參閱＜<a href="manage-role-groups-exchange-2013-help.md">管理角色群組</a>＞主題的＜將角色新增至角色群組＞一節。


如需在 Exchange 2013 中建立通訊清單的詳細指示，請參閱[建立通訊清單](create-an-address-list-exchange-2013-help.md)。如需在 Exchange Online 中建立通訊清單的詳細指示，請參閱[管理 Exchange Online 中的地址清單](https://technet.microsoft.com/zh-tw/library/jj983798\(v=exchg.150\))。

