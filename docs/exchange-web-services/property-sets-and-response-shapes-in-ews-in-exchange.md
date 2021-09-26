---
title: Eigenschaftensätze und Antwort shapes in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 04a29804-6067-48e7-9f5c-534e253a230e
description: Erfahren Sie, wie Sie die Antwort-Shapes und Eigenschaftensätze verwalten, die von der verwalteten EWS-API und EWS in Exchange zurückgegeben werden.
ms.openlocfilehash: 7720a07a6fd288f289bba371ce6fd8a6e349a8ce
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543849"
---
# <a name="property-sets-and-response-shapes-in-ews-in-exchange"></a>Eigenschaftensätze und Antwort shapes in EWS in Exchange

Erfahren Sie, wie Sie die Antwort-Shapes und Eigenschaftensätze verwalten, die von der verwalteten EWS-API und EWS in Exchange zurückgegeben werden.
  
Der Exchange Datenspeicher bietet eine flexible Speicherlösung, mit der Sie verschiedene Elemente, z. B. Kontakte und Kalendereinträge, im selben Ordner speichern können. Es kann jedoch schwierig sein, die Daten zu verwalten, die von einem Aufruf eines EWS-Vorgangs oder einer verwalteten EWS-API-Methode zurückgegeben werden.
  
Um das Verwalten der von Exchange Online zurückgegebenen Daten, Exchange Online als Teil Office 365 oder version von Excahange ab Exchange 2013 zu vereinfachen, verwendet die verwaltete EWS-API Eigenschaftensätze, und EWS verwendet Antwortshapes. Hierbei handelt es sich um vordefinierte Auflistungen, die die gängigsten Eigenschaften eines Speicherelements bereitstellen. Der zurückgegebene Eigenschaftensatz wird durch den Elementtyp bestimmt. Das bedeutet, dass Beim Binden eines Elements mithilfe der methode Exchange Managed API [Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) eine andere Gruppe von Eigenschaften abhängig vom Typ des Elements abgerufen wird, an das Sie binden. Die Bindung an ein Kalenderelement gibt einen anderen Satz von Eigenschaften zurück als die Bindung an ein Kontaktelement. Ebenso gibt der [GetItem-Vorgang](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) bei Verwendung von EWS einen anderen Satz von Eigenschaften basierend auf dem typ des zurückgegebenen Elements zurück. 
  
Durch das Binden an einen Ordner mit der [Folder.Bind-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) oder mithilfe des [GetFolder-Vorgangs](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) werden auch unterschiedliche Eigenschaftensätze basierend auf dem angeforderten Ordner zurückgegeben. 
  
**Tabelle 1. Vordefinierte Antwortshapes**

|**Antwort-Shape**|**Entsprechung in der verwalteten EWS-API**|**Beschreibung**|
|:-----|:-----|:-----|
|Nur ID  <br/> |[BasePropertySet.IdOnly](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) <br/> |Gibt nur den Bezeichner des Elements oder Ordners zurück. Die meisten Anwendungen sollten dieses Antwort-Shape verwenden und alle zusätzlichen Eigenschaften angeben, die erforderlich sind.  <br/> |
|Standard  <br/> |–  <br/> |Gibt einen vordefinierten Satz von Eigenschaften zurück, die die Standardeinstellung für das Element oder den Ordner sind (nur EWS).  <br/> |
|Alle Eigenschaften  <br/> |[BasePropertySet.FirstClassProperties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) <br/> |Gibt die Eigenschaften zurück, die von Clientanwendungen am häufigsten verwendet werden. Sie können zusätzliche Eigenschaften mithilfe eines Eigenschaftspfads zurückgeben.  <br/> |
   
## <a name="default-response-shapes"></a>Standardmäßige Antwortshapes

EWS enthält eine Reihe von Standardantwort-Shapes für Ordner und Elemente. 
  
In der folgenden Tabelle sind die Standardeigenschaften aufgeführt, die von den EWS-Vorgängen ["FindFolder"](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) und ["GetFolder"](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) für jeden Ordner zurückgegeben werden. 
  
**Tabelle 2. Standardordnereigenschaften**

|**Eigenschaft**|**Posteingang**|**Calendar**|**Kontakte**|**Gelöschte Elemente**|**Entwürfe**|**Hinweise**|**Andere Ordner**|**Postausgang**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Anzeigename  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Ordner-ID  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Anzahl der Unterordner  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Gesamtanzahl  <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Ungelesene Anzahl  <br/> |X  <br/> |||X  <br/> |X  <br/> ||X  <br/> |X  <br/> |
   
In der folgenden Tabelle sind die Standardeigenschaften aufgeführt, die von den EWS-Vorgängen [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) und [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) für jeden Elementtyp zurückgegeben werden. 
  
**Tabelle 3. Standardelementeigenschaften**

|**Eigenschaft**|**Kalenderelement**|**Kontaktelement**|**Nachrichtenelement**|**Aufgabenelement**|
|:-----|:-----|:-----|:-----|:-----|
|Text  <br/> |||X(1)  <br/> ||
|CalendarItemType  <br/> ||x  <br/> |||
|CompanyName  <br/> ||x  <br/> |||
|CompleteName  <br/> ||x  <br/> |||
|DateTimeCreated  <br/> |||x  <br/> ||
|DateTimeSent  <br/> |||x  <br/> ||
|DueDate  <br/> ||||x(2)  <br/> |
|EmailAddresses  <br/> ||x  <br/> |||
|Ende  <br/> |x  <br/> ||||
|FileAs  <br/> ||x  <br/> |||
|Von  <br/> |||x  <br/> ||
|HasAttachments  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ImAddresses  <br/> ||x  <br/> |||
|IsAssociated  <br/> |x  <br/> ||x  <br/> ||
|IsDeliveryReceiptRequested  <br/> |||x  <br/> ||
|ItemId  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|JobTitle  <br/> ||x  <br/> |||
|LegacyFreeBusyStatus  <br/> |x  <br/> ||||
|Ort  <br/> |x  <br/> ||||
|Organisator  <br/> |x  <br/> ||||
|PercentComplete  <br/> ||||x  <br/> |
|PhoneNumbers  <br/> ||x  <br/> |||
|PhysicalAddresses  <br/> ||x  <br/> |||
|ResponseObjects  <br/> |x(1)  <br/> ||x(1)  <br/> ||
|Empfindlichkeit  <br/> |||x  <br/> ||
|Size  <br/> |||x  <br/> ||
|StartDate  <br/> ||||x(2)  <br/> |
|Status  <br/> ||||x  <br/> |
|Betreff  <br/> |x  <br/> ||x  <br/> |x  <br/> |
   
Hinweise:
  
1. In der Antwort des **GetItem-Vorgangs** enthalten. Nicht in der Antwort des **FindItem-Vorgangs** enthalten. 
    
2. Nur in der Antwort enthalten, wenn das Feld Daten enthält. Nicht in der Antwort enthalten, wenn das Feld leer ist.
    
### <a name="all-properties-set-and-response-shape"></a>Alle Eigenschaften festgelegt und Antwort-Shape

In der folgenden Tabelle sind die Eigenschaften der ersten Klasse aufgeführt, die durch Aufrufen der verwalteten EWS-API-Methoden ["Item.Bind"](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) und ["Item.FindItems"](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) der verwalteten EWS-API zurückgegeben werden, sowie das Antwort-Shape "alle Eigenschaften", das von den EWS-Vorgängen ["FindItem"](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) und ["GetItem"](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) zurückgegeben wird. 
  
Sie können dem Eigenschaftensatz zusätzliche Eigenschaften hinzufügen oder erweiterte Eigenschaften einschließen. Ausführliche Informationen finden Sie unter [Eigenschaften und erweiterte Eigenschaften in EWS in Exchange.](properties-and-extended-properties-in-ews-in-exchange.md)
  
**Tabelle 4. First-Class-Eigenschaften**

|||||||
|:-----|:-----|:-----|:-----|:-----|:-----|
|Eigenschaft  <br/> |Kalenderelement  <br/> |Kontaktelement  <br/> |Nachrichtenelement  <br/> |Element posten  <br/> |Aufgabenelement  <br/> |
|ActualWork  <br/> |||||x  <br/> |
|AdjacentMeetingCount  <br/> |x  <br/> |||||
|AdjacentMeetings  <br/> |x  <br/> |||||
|Alias  <br/> ||x  <br/> ||||
|AllowNewTimeProposal  <br/> |x  <br/> |||||
|AppointmentReplyTime  <br/> |x  <br/> |||||
|AppointmentSequenceNumber  <br/> |x  <br/> |||||
|AppointmentState  <br/> |x  <br/> |||||
|AssignedTime  <br/> |||||x  <br/> |
|AssistantName  <br/> ||x  <br/> ||||
|BccRecipients  <br/> |||x  <br/> |||
|BillingInformation  <br/> |||||x  <br/> |
|Text  <br/> |x(1)  <br/> |x(1)  <br/> |x(1)  <br/> ||x(1)  <br/> |
|BusinessHomePage  <br/> ||x  <br/> |x  <br/> |||
|CalendarItemType  <br/> |x  <br/> |||||
|Categories  <br/> |x  <br/> ||x  <br/> |x  <br/> |x  <br/> |
|CcRecipients  <br/> |||x  <br/> |||
|ChangeCount  <br/> |||||x  <br/> |
|Untergeordnetes Element  <br/> ||x  <br/> ||||
|Unternehmen  <br/> |||||x  <br/> |
|CompleteDate  <br/> |||||x  <br/> |
|CompleteName  <br/> ||x  <br/> ||||
|ConferenceType  <br/> |x  <br/> |||||
|ConflictingMeetingCount  <br/> |x  <br/> |||||
|ConflictingMeetings  <br/> |x  <br/> |||||
|Kontakte  <br/> |||||x  <br/> |
|ContactSource  <br/> ||x  <br/> ||||
|ConversationId  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ConversationIndex  <br/> |||x  <br/> |x  <br/> ||
|ConversationTopic  <br/> |||x  <br/> |x  <br/> ||
|Culture  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DateTimeCreated  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DateTimeReceived  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DateTimeSent  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DateTimeStamp  <br/> |x  <br/> |||||
|DelegationState  <br/> |||||x  <br/> |
|Delegator  <br/> |||||x  <br/> |
|DeletedOccurrences  <br/> |x  <br/> |||||
|Abteilung  <br/> ||x  <br/> ||||
|DirectoryId  <br/> ||x  <br/> ||||
|DirectReports  <br/> ||x  <br/> ||||
|DisplayCc  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DisplayName  <br/> ||x  <br/> ||||
|DisplayTo  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DueDate  <br/> |||||x  <br/> |
|Dauer  <br/> |x  <br/> |||||
|EffectiveRights  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|EmailAddresses  <br/> ||x  <br/> ||||
|Ende  <br/> |x  <br/> |||||
|EndTimeZone  <br/> |x  <br/> |||||
|FileAs  <br/> ||x  <br/> ||||
|FileAsMapping  <br/> ||x  <br/> ||||
|FirstOccurrence  <br/> |x  <br/> |||||
|Von  <br/> |||x  <br/> |x  <br/> ||
|Generation  <br/> ||x  <br/> ||||
|GivenName  <br/> ||x  <br/> ||||
|HasAttachments  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|HasPicture  <br/> ||x  <br/> ||||
|ImAddresses  <br/> ||x  <br/> ||||
|Importance  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|Initialen  <br/> ||x  <br/> ||||
|InReplyTo  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|InternetMessageId  <br/> |||x  <br/> |x  <br/> ||
|InternetMessageHeaders  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsAllDayEvent  <br/> |x  <br/> |||||
|IsAssociated  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsCancelled  <br/> |x  <br/> |||||
|IsComplete  <br/> |||||x  <br/> |
|IsDeliveryReceiptRequested  <br/> |||x  <br/> |||
|IsDraft  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsFromMe  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsMeeting  <br/> |x  <br/> |||||
|IsOnlineMeeting  <br/> |x  <br/> |||||
|IsRead  <br/> |||x  <br/> |||
|IsReadReceiptRequested  <br/> |||x  <br/> |||
|IsRecurring  <br/> |x  <br/> ||||x  <br/> |
|IsResend  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsResponseRequested  <br/> |x  <br/> ||x  <br/> |||
|IsSubmitted  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsUnmodified  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ItemClass  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ItemId  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|JobTitle  <br/> ||x  <br/> ||||
|LastModifiedName  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|LastModifiedTime  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|LastOccurrance  <br/> |x  <br/> |||||
|LegacyFreeBusyStatus  <br/> |x  <br/> |||||
|Ort  <br/> |x  <br/> |||||
|Manager  <br/> ||x  <br/> ||||
|MeetingRequestWasSent  <br/> |x  <br/> |||||
|MeetingTimeZone  <br/> |x  <br/> |||||
|MeetingWorkspaceUrl  <br/> |x  <br/> |||||
|MiddleName  <br/> ||x  <br/> ||||
|Reisekilometer  <br/> ||x  <br/> |||x  <br/> |
|ModifiedOccurrances  <br/> |x  <br/> |||||
|MyResponseType  <br/> |x  <br/> |||||
|NetShowUrl  <br/> |x  <br/> |||||
|NickName  <br/> ||x  <br/> ||||
|Notizen  <br/> ||x  <br/> ||||
|OfficeLocation  <br/> ||x  <br/> ||||
|OptionalAttendees  <br/> |x  <br/> |||||
|Organisator  <br/> |x  <br/> |||||
|OriginalStart  <br/> |x  <br/> |||||
|Besitzer  <br/> |||||x  <br/> |
|ParentFolderId  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|PercentComplete  <br/> |||||x  <br/> |
|PhoneNumbers  <br/> ||x  <br/> ||||
|PhoneticFirstName  <br/> ||x  <br/> ||||
|PhoneticFullName  <br/> ||x  <br/> ||||
|PhoneticLastName  <br/> ||x  <br/> ||||
|Foto  <br/> ||x  <br/> ||||
|PhysicalAddresses  <br/> ||x  <br/> ||||
|PostalAddressIndex  <br/> ||x  <br/> ||||
|PostedTime  <br/> ||||x  <br/> ||
|Beruf  <br/> ||x  <br/> ||||
|ReceivedBy  <br/> |||x  <br/> |||
|ReceivedRepresenting  <br/> |||x  <br/> |||
|Reccurrence  <br/> |x  <br/> ||||x  <br/> |
|Informationsquellen  <br/> |||x  <br/> |x  <br/> ||
|ReminderDueBy  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ReminderIsSet  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ReminderMinutesBeforeStart  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ReplyTo  <br/> |||x  <br/> |||
|RequiredAttendees  <br/> |x  <br/> |||||
|Ressourcen  <br/> |x  <br/> |||||
|ResponseObjects  <br/> |x(1)  <br/> |x(1)  <br/> |x(1)  <br/> |x(1)  <br/> |x(1)  <br/> |
|Absender  <br/> |||x  <br/> |x  <br/> ||
|Vertraulichkeit  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|Size  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|SpouseName  <br/> ||x  <br/> ||||
|Start  <br/> |x  <br/> |||||
|StartDate  <br/> |||||x  <br/> |
|StartTimeZone  <br/> |x  <br/> |||||
|Status  <br/> |||||x  <br/> |
|StatusDescription  <br/> |||||x  <br/> |
|Betreff  <br/> |x  <br/> |x  <br/> |x  <br/> ||x  <br/> |
|Nachname  <br/> ||x  <br/> ||||
|TimeZone  <br/> |x  <br/> |||||
|ToRecipients  <br/> |||x  <br/> |||
|TotalWork  <br/> |||||x  <br/> |
|WebClientEditFormQueryString  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|WebClientReadFormQueryString  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
   
Hinweise:
  
1. Enthalten bei der [Bindung an ein Element](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) und in der Antwort des [GetItem-Vorgangs.](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) Nicht im Ergebnis der [Item.FindItems-Methode](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) oder in der Antwort des [FindItem-Vorgangs](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)enthalten.
    
## <a name="see-also"></a>Siehe auch

- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [FindItem-Vorgang](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
- [GetItem-Vorgang](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)
    
- [FindFolder-Vorgang](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [GetFolder-Vorgang](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)
    

