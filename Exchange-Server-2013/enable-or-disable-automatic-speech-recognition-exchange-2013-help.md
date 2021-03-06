﻿---
title: '啟用或停用自動語音辨識: Exchange Online Help'
TOCTitle: 啟用或停用自動語音辨識
ms:assetid: 92b3b679-b503-4068-8e88-25ec0f4537ab
ms:mtpsurl: https://technet.microsoft.com/zh-tw/library/Bb232128(v=EXCHG.150)
ms:contentKeyID: 52062354
ms.date: 05/23/2018
mtps_version: v=EXCHG.150
ms.translationtype: MT
---

# 啟用或停用自動語音辨識

 

_**適用版本：** Exchange Online, Exchange Server 2013, Exchange Server 2016_

_**上次修改主題的時間：** 2012-12-12_

您可以啟用整合通訊 (UM) 自動語音應答的自動語音辨識 (ASR)。您語音啟用功能之後 UM 自動語音應答、 來電者可以自動語音應答提示口頭回應並瀏覽自動語音應答功能表系統。根據預設，自動語音應答未啟用語音的當您建立。您語音啟用功能之後的自動語音應答，來電者可以使用僅限語音命令來瀏覽自動語音應答功能表系統並不能使用按鍵式輸入。

雖然不需要是，我們建議您讓來電者可以使用按鍵式輸入啟用語音的自動語音應答無法辨識或不了解這些說出字設定每個啟用語音的自動語音應答雙音多頻 (dtmf) 後援自動語音應答。如果已設定 DTMF 後援自動語音應答、 來電者可以使用 DTMF 輸入，也稱為按鍵式輸入來瀏覽自動語音應答功能表系統、 拼字使用者的名稱或使用自訂的功能表提示。我們不建議的您啟用語音 DTMF 後援自動語音應答。

如需與 UM 自動語音應答相關的其他管理工作，請參閱[UM 自動語音應答程序](um-auto-attendant-procedures-exchange-2013-help.md)。

## 開始之前有哪些須知？

  - 預估完成時間： 少於 1 分鐘。

  - 您必須已獲指派權限，才能執行此程序或這些程序。若要查看您需要的權限，請參閱 [整合的通訊權限](unified-messaging-permissions-exchange-2013-help.md)主題中的「UM 自動語音應答」項目。

  - 在執行這些程序之前，請確認已建立 UM 撥號對應表。如需詳細步驟，請參閱[建立 UM 撥號對應表](create-a-um-dial-plan-exchange-2013-help.md)。

  - 在執行這些程序之前，請確認已建立 UM 自動語音應答。 如需詳細步驟，請參閱[建立 UM 自動語音應答](create-a-um-auto-attendant-exchange-2013-help.md)。

  - 如需適用於此主題中程序的快速鍵相關資訊，請參閱 [Exchange 系統管理中心的鍵盤快速鍵](keyboard-shortcuts-in-the-exchange-admin-center-exchange-online-protection-help.md)。


> [!TIP]  
> 有問題嗎？在 Exchange 論壇中尋求協助。 論壇的網址為：<a href="https://go.microsoft.com/fwlink/p/?linkid=60612">Exchange Server</a>、 <a href="https://go.microsoft.com/fwlink/p/?linkid=267542">Exchange Online</a> 或 <a href="https://go.microsoft.com/fwlink/p/?linkid=285351">Exchange Online Protection</a>。.




## 您要執行的工作

## 使用 EAC 啟用 UM 自動語音應答的語音功能

1.  在 EAC 中，瀏覽至 \[整合通訊\] \> \[UM 撥號對應表\]。在清單檢視中，選取您要變更的 UM 撥號對應表，然後按一下 \[編輯\]![編輯圖示](images/JJ218640.6f53ccb2-1f13-4c02-bea0-30690e6ea71d(EXCHG.150).gif "編輯圖示")。

2.  在 **\[UM 撥號對應表\]** 頁面的 **\[UM 自動語音應答\]** 下方，選取您要啟用語音的 UM 自動語音應答，然後按一下 **\[編輯\]**![編輯圖示](images/JJ218640.6f53ccb2-1f13-4c02-bea0-30690e6ea71d(EXCHG.150).gif "編輯圖示")。

3.  在 \[ **UM 自動語音應答**\] 頁面上 \>**一般**、 選取可讓語音辨識的 \[**設定以回應語音命令的自動語音應答**\] 旁的核取方塊。若要停用自動語音辨識，請清除此核取方塊。

4.  按一下 **\[儲存\]**。

## 使用命令介面啟用 UM 自動語音應答的語音功能

此範例會在名為 `MySpeechEnabled AA` 的 UM 自動語音應答上啟用 ASR。

    Set-UMAutoAttendant -Identity MySpeechEnabledAA -SpeechEnabled $true

