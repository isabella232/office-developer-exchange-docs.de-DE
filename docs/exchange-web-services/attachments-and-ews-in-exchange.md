---
title: Attachments and EWS in Exchange
manager: sethgros
ms.date: 7/11/2016
ms.audience: Developer
ms.assetid: 8e4289a4-ec9d-4502-9854-c593c95d5f98
description: Erfahren Sie mehr über Anlagen und wie Ihre verwaltete EWS-API oder EWS im Exchange-Client diese darstellen.
localization_priority: Priority
ms.openlocfilehash: d37fef9ea14a3b42a0eed0240724fe69c8531c93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528489"
---
# <a name="attachments-and-ews-in-exchange"></a>Attachments and EWS in Exchange

Erfahren Sie mehr über Anlagen und wie Ihre verwaltete EWS-API oder EWS im Exchange-Client diese darstellen.
  
Normalerweise werden Anlagen e-Mail-Elementen zugeordnet, aber tatsächlich können alle EWS-Elemente – e-Mail-Nachrichten, Kalenderelemente, Kontakte, Aufgaben – Anlagen enthalten.
  
## <a name="types-of-attachments"></a>Anlagentypen

In EWS werden Anlagen in zwei Gruppen kategorisiert: Dateianlagen und Element Anlagen.
  
- **Element Anlagen:** Stark typisierte [EWS-Elemente](folders-and-items-in-ews-in-exchange.md)wie e-Mail-Nachrichten und Kalenderelemente, die an ein anderes streng typisiertes EWS-Element angefügt sind. Ein beliebiges stark typisiertes Element, das mit dem verwaltete EWS-API oder EWS erstellt werden kann, kann als Elementanlage verwendet werden. Der Inhalt einer Elementanlage ist das stark typisierte Element, das einen einfachen Zugriff auf alle Eigenschaften ermöglicht. Element Anlagen können eigene Element Anlagen haben, daher ist eine Hierarchie von Element Anlagen (oder Verschachteln von Anlagen) möglich.
    
- **Dateianlagen:** Jede Datei, beispielsweise a. txt,. jpg,. zip,. PDF oder sogar eine msg-Datei. Eine Dateianlage hat nur einige Eigenschaften, von denen einer der Base-64-codierte Inhalt der Datei ist. 
    
- **Referenzanlagen:** Alle Anlagen, auf die von einem Datei Anbieter verwiesen wird, beispielsweise eine Datei, die sich in der Cloud befindet. Eine Anlage kann von mehreren Anbietern sein. 
    
Wenn Sie Anlagen von einem Element hinzufügen oder abrufen, wird dies je nachdem, ob es sich um eine Dateianlage oder um eine Elementanlage handelt, anders gehandhabt. Wenn Sie beispielsweise eine Dateianlage zu einem Element hinzufügen möchten, können Sie einfach den Speicherort der Datei übergeben. Um ein vorhandenes Element als Elementanlage hinzuzufügen, müssen Sie die Eigenschaften oder den MIME-Inhalt des vorhandenen Elements tatsächlich in eine neue Elementanlage kopieren. Sie können nicht einfach an das vorhandene Element binden. Die Unterscheidung zwischen den beiden Anlagentypen ist daher wichtig. Weitere Details zu den Unterschieden zwischen Element Anlagen und Dateianlagen werden in den Artikeln [in diesem Abschnitt](#bk_inthissection)erläutert.
  
## <a name="how-are-attachments-represented-programmatically"></a>Wie werden Anlagenprogramm gesteuert dargestellt?

Anlagen werden in einer Auflistung des EWS-Elements gespeichert. Die Attachments-Auflistung besteht aus Dateianlagen und/oder Element Anlagen. Metadaten zur Anlagensammlung sind verfügbar, wenn Sie ein Element mithilfe der verwaltete EWS-API [Item. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) -Methode oder der EWS- [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) -Operation abrufen, aber zusätzliche Aufrufe sind erforderlich, um den Inhalt der Anlagen tatsächlich abzurufen. 
  
**Tabelle 1. Elementmetadaten zu Anlagen**

|**Metadata-Entität**|**Eigenschaft in der verwalteten EWS-API**|**EWS-Element**|
|:-----|:-----|:-----|
|Anlagen Kennzeichen (Inline Anlagen werden nicht markiert)  <br/> |[Item. hasattachments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) <br/> |[HasAttachments](https://msdn.microsoft.com/library/538b7a85-11d7-4daa-8458-09b540760e8b%28Office.15%29.aspx) <br/> |
|Attachment-Sammlung  <br/> |[Item. Attachments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx) <br/> |[Anlagen](https://msdn.microsoft.com/library/b470e614-34bb-44f0-8790-7ddbdcbbd29d%28Office.15%29.aspx) <br/> |
|Anlagen-ID  <br/> |[Attachment.Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.id%28v=exchg.80%29.aspx) <br/> |[AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) <br/> |
   
**Tabelle 2. Attachment-Entitäten**

|**Attachment-Typ**|**Verwaltete EWS-API-Klasse**|**EWS-Element**|
|:-----|:-----|:-----|
|Dateianlage  <br/> |[FileAttachment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.fileattachment%28v=exchg.80%29.aspx) <br/> |[FileAttachment](https://msdn.microsoft.com/library/3ecea174-73d1-47fd-8917-6065cef1d565%28Office.15%29.aspx) <br/> |
|Elementanlage  <br/> |[ItemAttachment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemattachment%28v=exchg.80%29.aspx) <br/> [ItemAttachment\<TItem\>](https://msdn.microsoft.com/library/dd635165%28v=exchg.80%29.aspx) <br/> |[ItemAttachment](https://msdn.microsoft.com/library/089ee599-f45e-46f5-a18a-5cfb3d2851ff%28Office.15%29.aspx) <br/> |
|Verweisanlage  <br/> |[ReferenceAttachmentType complexType (EWS)](https://msdn.microsoft.com/library/18bfa012-e903-d7f3-528a-31ccceb65463%28Office.15%29.aspx) <br/> |[ReferenceAttachment](https://msdn.microsoft.com/library/b9bde862-6b75-4a81-8033-00a47be4dc2f%28Office.15%29.aspx) <br/> |
   
## <a name="inline-attachments"></a>Inline Anlagen

Inline Anlagen sind eine besondere Brutanlage. Sowohl Dateianlagen als auch Element Anlagen können Inline Anlagen sein. Eine Inline Anlage wird als Teil des Textkörper Inhalts angezeigt und behält ihre Position relativ zum restlichen Inhalt des Elements bei. 
  
Eine Anlage ist eine Inline Anlage, wenn die verwaltete EWS-API [IsInline](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.isinline%28v=exchg.80%29.aspx) -Eigenschaft oder das EWS- [IsInline](https://msdn.microsoft.com/library/5e7712c8-372a-4a16-be64-360c5ff3961a%28Office.15%29.aspx) -Element auf true festgelegt ist. Inline Anlagen verwenden Sie die folgenden optionalen Eigenschaften und Elemente, um den Speicherort einer Inline Anlage zu identifizieren: 
  
- Verwaltete EWS-API – [Inhalts](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.contentid%28v=exchg.80%29.aspx) -oder [ContentLocation](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.contentlocation%28v=exchg.80%29.aspx) -Eigenschaften. 
    
- EWS – [Inhalts](https://msdn.microsoft.com/library/bc59100d-6079-414b-a6e0-7c15feaa3184%28Office.15%29.aspx) -oder [ContentLocation](https://msdn.microsoft.com/library/d91cf587-24e3-4c13-8784-5ca29787cca7%28Office.15%29.aspx) -Element. 
    
Beachten Sie, dass die verwaltete EWS-API [hasattachments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) -Eigenschaft und das EWS- [hasattachments](https://msdn.microsoft.com/library/538b7a85-11d7-4daa-8458-09b540760e8b%28Office.15%29.aspx) -Element nicht das vorhanden sein von Inline Anlagen widerspiegeln, weshalb Inline Anlagen auch als versteckte Anlagen bezeichnet werden. Wenn Sie also die verwaltete EWS-API [IsInline](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.isinline%28v=exchg.80%29.aspx) -Eigenschaft oder das EWS- [IsInline](https://msdn.microsoft.com/library/5e7712c8-372a-4a16-be64-360c5ff3961a%28Office.15%29.aspx) -Element auf true festlegen und das Element keine anderen Anlagen aufweist, wird **hasattachments** auf false festgelegt. Wenn Ihr Client **hasattachments** verwendet, um einen Anlagen Indikator oder ein Symbol in einer e-Mail aufzufüllen, beachten Sie, dass das Symbol nicht für e-Mails mit Inline Anlagen angezeigt wird. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_inthissection"> </a>

- [Hinzufügen von Anlagen mithilfe von EWS in Exchange](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [Abrufen von Anlagen mithilfe von EWS in Exchange](how-to-get-attachments-by-using-ews-in-exchange.md)
    
- [Löschen von Anlagen mithilfe von EWS in Exchange](how-to-delete-attachments-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Siehe auch
<a name="bk_additionalresources"> </a>

- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Ordner und Elemente in EWS in Exchange](folders-and-items-in-ews-in-exchange.md)
    
- [E-Mail- und EWS in Exchange](email-and-ews-in-exchange.md)
    

