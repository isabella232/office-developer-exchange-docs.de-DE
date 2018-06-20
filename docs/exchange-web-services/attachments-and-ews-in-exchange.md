---
title: Anlagen und EWS in Exchange
manager: sethgros
ms.date: 7/11/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e4289a4-ec9d-4502-9854-c593c95d5f98
description: Informationen Sie zu Anlagen und wie Ihre EWS Managed API oder EWS in Exchange Client diese darstellt.
ms.openlocfilehash: e4a97873798b8252e6fc14003519ce8a0eab7ec8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756821"
---
# <a name="attachments-and-ews-in-exchange"></a>Anlagen und EWS in Exchange

Informationen Sie zu Anlagen und wie Ihre EWS Managed API oder EWS in Exchange Client diese darstellt.
  
In der Regel Anlagen e-Mail-Elemente, aber tatsächlich alle EWS-Elemente zugeordnet sind – e-Mail-Nachrichten, Kalenderelemente, Kontakte, Aufgaben – können Anlagen enthalten.
  
## <a name="types-of-attachments"></a>Typen von Anlagen

EWS Anlagen in zwei Gruppen kategorisiert:-Anlagen und Anlagen.
  
- **Element Anlagen:** Stark typisierten [EWS-Elementen](folders-and-items-in-ews-in-exchange.md), wie e-Mail-Nachrichten und Kalenderelemente, die mit einem anderen stark typisierten EWS-Element zugeordnet sind. Alle stark typisierten-Element, das mithilfe des EWS Managed API oder EWS erstellt werden kann, kann als Elementanlage verwendet werden. Der Inhalt von Elementanlage ist das Element stark typisierten, das einfachen Zugriff auf alle Eigenschaften bereitstellt. Elementanlagen können ihre eigenen elementanlagen haben, damit eine Hierarchie von Anlagen (oder Verschachtelung von Anlagen) möglich ist.
    
- **Dateianlagen:** Jede Datei, wie einer einer TXT, JPG, ZIP, PDF, oder sogar eine MSG-Datei. Eine Dateianlage hat nur ein paar Eigenschaften, von denen die Base64-codierten Inhalt der Datei ist. 
    
- **Verweisen auf Anlagen:** Mindestens eine Anlage, die von einem Anbieter Datei, wie etwa einer Datei befindet sich in der Cloud verwiesen wird. Eine Anlage kann von mehreren Anbietern sein. 
    
Wenn Sie hinzufügen oder Abrufen von Anlagen aus einem Element, dafür Sie gibt es unterschiedlich je nachdem, ob es sich um eine Dateianlage oder Elementanlage handelt. Beispielsweise können eine Dateianlage für ein Element hinzuzufügen, übergeben Sie einfach in den Speicherort der Datei. Um ein vorhandenes Element als Elementanlage hinzuzufügen, müssen Sie tatsächlich die Eigenschaften oder dem MIME-Inhaltstyp, der das vorhandene Element in eine neue Anlage Element zu kopieren. Sie können nicht nur an das vorhandene Element binden. Es ist wichtig, also Unterscheidung zwischen den beiden Typen von Anlagen. Weitere Informationen zu den Unterschieden zwischen elementanlagen und Dateianlagen werden in den Artikeln [In diesem Abschnitt](#bk_inthissection)erläutert.
  
## <a name="how-are-attachments-represented-programmatically"></a>Wie werden Anlagen programmgesteuert werden dargestellt?

Anlagen werden in einer Auflistung auf das EWS-Element gespeichert. Attachments-Auflistung Dateianlagen und/oder elementanlagen besteht. Metadaten für die Auflistung der Anhänge ist verfügbar, wenn Sie ein Element mit der EWS Managed API [Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) -Methode oder die EWS [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) Operation abrufen, jedoch zusätzliche Aufrufe erforderlich sind, um den Inhalt der Anlagen tatsächlich abzurufen. 
  
**In Tabelle 1. Elementmetadaten zu Anlagen**

|**Metadaten-Entität**|**Eigenschaft in der verwalteten EWS-API**|**EWS-Element**|
|:-----|:-----|:-----|
|Anlage-Symbol (nicht Inlineanlage gekennzeichnet)  <br/> |[Item.HasAttachments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) <br/> |[HasAttachments](http://msdn.microsoft.com/library/538b7a85-11d7-4daa-8458-09b540760e8b%28Office.15%29.aspx) <br/> |
|Anlage-Auflistung  <br/> |[Item.Attachments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx) <br/> |[Anlagen](http://msdn.microsoft.com/library/b470e614-34bb-44f0-8790-7ddbdcbbd29d%28Office.15%29.aspx) <br/> |
|Anlagen-ID  <br/> |[Attachment.Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachment.id%28v=exchg.80%29.aspx) <br/> |[AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) <br/> |
   
**In Tabelle 2. Anlage Entitäten**

|**Anlagetyp**|**Verwaltete EWS-API-Klasse**|**EWS-Element**|
|:-----|:-----|:-----|
|Dateianlage  <br/> |[FileAttachment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.fileattachment%28v=exchg.80%29.aspx) <br/> |[FileAttachment](http://msdn.microsoft.com/library/3ecea174-73d1-47fd-8917-6065cef1d565%28Office.15%29.aspx) <br/> |
|Element-Anlage  <br/> |[ItemAttachment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemattachment%28v=exchg.80%29.aspx) <br/> [ItemAttachment\<TItem\>](http://msdn.microsoft.com/en-us/library/dd635165%28v=exchg.80%29.aspx) <br/> |[ItemAttachment](http://msdn.microsoft.com/library/089ee599-f45e-46f5-a18a-5cfb3d2851ff%28Office.15%29.aspx) <br/> |
|Verweisanlage  <br/> |[ReferenceAttachmentType ComplexType (EWS)](http://msdn.microsoft.com/library/18bfa012-e903-d7f3-528a-31ccceb65463%28Office.15%29.aspx) <br/> |[ReferenceAttachment](http://msdn.microsoft.com/library/b9bde862-6b75-4a81-8033-00a47be4dc2f%28Office.15%29.aspx) <br/> |
   
## <a name="inline-attachments"></a>Inline-Anlagen

Inline-Anlagen sind eine spezielle branchenführende Anlage. Beide Dateianlagen und die Anlagen Inlineanlage werden können. Eine Inlineanlage wird als Teil des Inhalts Body und behält die Position relativ zu den Rest des Inhalts im Element. 
  
Eine Anlage eine Inlineanlage ist, wenn die EWS Managed API [IsInline](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachment.isinline%28v=exchg.80%29.aspx) -Eigenschaft oder das EWS [IsInline](http://msdn.microsoft.com/library/5e7712c8-372a-4a16-be64-360c5ff3961a%28Office.15%29.aspx) -Element festgelegt ist auf "true". Inline-Anlagen verwenden die folgenden optionalen Eigenschaften und Elemente, um den Speicherort der eine Inlineanlage identifizieren: 
  
- EWS Managed API – [ContentId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachment.contentid%28v=exchg.80%29.aspx) oder [ContentLocation](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachment.contentlocation%28v=exchg.80%29.aspx) -Eigenschaften. 
    
- EWS – [ContentId](http://msdn.microsoft.com/library/bc59100d-6079-414b-a6e0-7c15feaa3184%28Office.15%29.aspx) oder [ContentLocation](http://msdn.microsoft.com/library/d91cf587-24e3-4c13-8784-5ca29787cca7%28Office.15%29.aspx) -Element. 
    
Beachten Sie, dass die EWS Managed API [HasAttachments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) -Eigenschaft und die EWS- [HasAttachments](http://msdn.microsoft.com/library/538b7a85-11d7-4daa-8458-09b540760e8b%28Office.15%29.aspx) -Element das Vorhandensein nicht wider Inlineanlage und, hat Anlagen ausgeblendet Warum Inlineanlage auch aufgerufen werden. Wenn Sie die EWS Managed API [IsInline](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachment.isinline%28v=exchg.80%29.aspx) -Eigenschaft oder das EWS [IsInline](http://msdn.microsoft.com/library/5e7712c8-372a-4a16-be64-360c5ff3961a%28Office.15%29.aspx) -Element auf "true" festgelegt, und das Element keine anderen Anlagen wurde, **HasAttachments** auf False festgelegt wird. Wenn der Client **HasAttachments** zum Auffüllen einer Anlage Symbol oder auf der Symbolleiste auf eine e-Mail verwendet wird, achten Sie darauf, dass das Symbol für e-Mails mit Inlineanlage nicht angezeigt wird. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_inthissection"> </a>

- [Hinzufügen von Anlagen im Exchange mithilfe der Exchange-Webdienste](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [Abrufen von Anlagen im Exchange mithilfe der Exchange-Webdienste](how-to-get-attachments-by-using-ews-in-exchange.md)
    
- [Löschen von Anlagen mithilfe der EWS in Exchange](how-to-delete-attachments-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Siehe auch
<a name="bk_additionalresources"> </a>

- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Ordner und Elemente in EWS in Exchange](folders-and-items-in-ews-in-exchange.md)
    
- [E-Mail- und EWS in Exchange](email-and-ews-in-exchange.md)
    

