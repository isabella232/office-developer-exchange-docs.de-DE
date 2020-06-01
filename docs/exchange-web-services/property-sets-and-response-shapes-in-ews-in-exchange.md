---
title: Eigenschaftensätze und Antwortshapes in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 04a29804-6067-48e7-9f5c-534e253a230e
description: Hier erfahren Sie, wie Sie die Antwort-Shapes und Eigenschaftensätze verwalten, die von der verwalteten EWS-API und EWS in Exchange zurückgegeben werden.
ms.openlocfilehash: 8f539a2131798e764574ef92f75deb654c02c90f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457662"
---
# <a name="property-sets-and-response-shapes-in-ews-in-exchange"></a>Eigenschaftensätze und Antwortshapes in EWS in Exchange

Hier erfahren Sie, wie Sie die Antwort-Shapes und Eigenschaftensätze verwalten, die von der verwalteten EWS-API und EWS in Exchange zurückgegeben werden.
  
Der Exchange-Datenspeicher bietet eine flexible Speicherlösung, mit der Sie unterschiedliche Elemente wie Kontakte und Kalendereinträge im gleichen Ordner speichern können. Es kann jedoch schwierig sein, die Daten zu verwalten, die von einem Anruf an einen EWS-Vorgang oder eine verwaltete EWS-API-Methode zurückgegeben werden.
  
Um die Verwaltung von Daten zu vereinfachen, die von Exchange Online zurückgegeben werden, Exchange Online im Rahmen von Office 365 oder Version von Excahange, beginnend mit Exchange 2013, verwendet der verwaltete EWS-API Eigenschaftensätze, und EWS verwendet Antwort-Shapes. Hierbei handelt es sich um vordefinierte Auflistungen, die die am häufigsten verwendeten Eigenschaften eines Store-Elements bereitstellen. Der Satz von Eigenschaften, der zurückgegeben wird, wird durch den Elementtyp bestimmt. Das bedeutet, dass Sie, wenn Sie ein Element mithilfe der Exchange Managed API [Item. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) -Methode binden, je nach Typ des Elements, an das Sie eine Bindung herstellen, einen anderen Satz von Eigenschaften erhalten. Durch das Binden an ein Kalenderelement wird ein anderer Eigenschaftensatz als das Binden an ein Kontaktelement zurückgegeben. Wenn Sie EWS verwenden, gibt der [GetItem-Vorgang](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) entsprechend dem Typ des zurückgegebenen Elements einen anderen Satz von Eigenschaften zurück. 
  
Durch das Binden an einen Ordner mit der [Folder. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) -Methode oder mit dem [GetFolder-Vorgang](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) werden auch unterschiedliche Eigenschaftensätze basierend auf dem von Ihnen angeforderten Ordner zurückgegeben. 
  
**Tabelle 1. Vordefinierte Antwort-Shapes**

|**Antwort-Shape**|**Entsprechung in der verwalteten EWS-API**|**Beschreibung**|
|:-----|:-----|:-----|
|Nur ID  <br/> |[BasePropertySet. IdOnly](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) <br/> |Gibt nur den Bezeichner des Elements oder Ordners zurück. Die meisten Anwendungen sollten dieses Antwort-Shape verwenden und zusätzliche Eigenschaften angeben, die erforderlich sind.  <br/> |
|Standard  <br/> |–  <br/> |Gibt eine vordefinierte Gruppe von Eigenschaften zurück, die der Standardwert für das Element oder den Ordner sind (nur EWS).  <br/> |
|Alle Eigenschaften  <br/> |[BasePropertySet. FirstClassProperties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) <br/> |Gibt die Eigenschaften zurück, die von Clientanwendungen am häufigsten verwendet werden. Sie können zusätzliche Eigenschaften mithilfe eines Eigenschaftenpfads zurückgeben.  <br/> |
   
## <a name="default-response-shapes"></a>Standardmäßige Antwortshapes

EWS enthält eine Reihe von standardmäßigen Antwort-Shapes für Ordner und Elemente. 
  
In der folgenden Tabelle sind die Standardeigenschaften aufgeführt, die für jeden Ordner durch die [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) -und [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) -EWS-Vorgänge zurückgegeben werden. 
  
**Tabelle 2. Standardordnereigenschaften**

|**Eigenschaft**|**Posteingang**|**Calendar**|**Kontakte**|**Gelöschte Elemente**|**Entwürfe**|**Hinweise**|**Andere Ordner**|**Postausgang**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Distinguished Name (DN)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Ordner-ID  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Unterordner Anzahl  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Gesamtanzahl  <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Ungelesene Anzahl  <br/> |X  <br/> |||X  <br/> |X  <br/> ||X  <br/> |X  <br/> |
   
In der folgenden Tabelle sind die Standardeigenschaften aufgeführt, die für jeden Elementtyp von den [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) -und [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) -EWS-Vorgängen zurückgegeben werden. 
  
**Tabelle 3. Standardelement Eigenschaften**

|**Eigenschaft**|**Kalenderelement**|**Kontaktelement**|**Nachrichtenelement**|**Aufgabenelement**|
|:-----|:-----|:-----|:-----|:-----|
|Body  <br/> |||X (1)  <br/> ||
|CalendarItemType  <br/> ||x  <br/> |||
|CompanyName  <br/> ||x  <br/> |||
|Completename  <br/> ||x  <br/> |||
|DateTimeCreated  <br/> |||x  <br/> ||
|DateTimeSent  <br/> |||x  <br/> ||
|DueDate  <br/> ||||x (2)  <br/> |
|EmailAddresses  <br/> ||x  <br/> |||
|Ende  <br/> |x  <br/> ||||
|FileAs  <br/> ||x  <br/> |||
|Von  <br/> |||x  <br/> ||
|HasAttachments  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|Imaddresses  <br/> ||x  <br/> |||
|Isassociated  <br/> |x  <br/> ||x  <br/> ||
|IsDeliveryReceiptRequested  <br/> |||x  <br/> ||
|Itemid  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|JobTitle  <br/> ||x  <br/> |||
|LegacyFreeBusyStatus  <br/> |x  <br/> ||||
|Standort  <br/> |x  <br/> ||||
|Organisator  <br/> |x  <br/> ||||
|PercentComplete  <br/> ||||x  <br/> |
|PhoneNumbers  <br/> ||x  <br/> |||
|PhysicalAddresses  <br/> ||x  <br/> |||
|ResponseObjects  <br/> |x (1)  <br/> ||x (1)  <br/> ||
|Sensitity  <br/> |||x  <br/> ||
|Größe  <br/> |||x  <br/> ||
|StartDate  <br/> ||||x (2)  <br/> |
|Status  <br/> ||||x  <br/> |
|Betreff  <br/> |x  <br/> ||x  <br/> |x  <br/> |
   
Hinweise:
  
1. In der Antwort vom **GetItem** -Vorgang enthalten. Nicht in der Antwort des **FindItem** -Vorgangs enthalten. 
    
2. Nur in der Antwort enthalten, wenn das Feld Daten enthält. Nicht in der Antwort enthalten, wenn das Feld leer ist.
    
### <a name="all-properties-set-and-response-shape"></a>Alle Eigenschaften festgelegt und Antwort-Shape

In der folgenden Tabelle sind die Eigenschaften der ersten Klasse aufgeführt, die durch Aufrufen der verwaltete EWS-API [Item. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) -und [Item. FindItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) -verwaltete EWS-API-Methoden und des Antwort-Shapes "All Properties" zurückgegeben werden, das von den [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) -und [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) -EWS-Vorgängen zurückgegeben wird. 
  
Sie können dem Eigenschaftenset zusätzliche Eigenschaften hinzufügen oder erweiterte Eigenschaften einschließen. Ausführliche Informationen finden Sie unter [Properties and Extended Properties in EWS in Exchange](properties-and-extended-properties-in-ews-in-exchange.md).
  
**Tabelle 4. Erstklassige Eigenschaften**

|||||||
|:-----|:-----|:-----|:-----|:-----|:-----|
|Eigenschaft  <br/> |Kalenderelement  <br/> |Kontaktelement  <br/> |Nachrichtenelement  <br/> |Posten Element  <br/> |Aufgabenelement  <br/> |
|ActualWork  <br/> |||||x  <br/> |
|AdjacentMeetingCount  <br/> |x  <br/> |||||
|AdjacentMeetings  <br/> |x  <br/> |||||
|Alias  <br/> ||x  <br/> ||||
|AllowNewTimeProposal  <br/> |x  <br/> |||||
|AppointmentReplyTime  <br/> |x  <br/> |||||
|AppointmentSequenceNumber  <br/> |x  <br/> |||||
|AppointmentState  <br/> |x  <br/> |||||
|Zugewiesenezeit  <br/> |||||x  <br/> |
|AssistantName  <br/> ||x  <br/> ||||
|BccRecipients  <br/> |||x  <br/> |||
|BillingInformation  <br/> |||||x  <br/> |
|Body  <br/> |x (1)  <br/> |x (1)  <br/> |x (1)  <br/> ||x (1)  <br/> |
|BusinessHomePage  <br/> ||x  <br/> |x  <br/> |||
|CalendarItemType  <br/> |x  <br/> |||||
|Kategorien  <br/> |x  <br/> ||x  <br/> |x  <br/> |x  <br/> |
|CcRecipients  <br/> |||x  <br/> |||
|ChangeCount  <br/> |||||x  <br/> |
|Untergeordnetes Element  <br/> ||x  <br/> ||||
|Unternehmen  <br/> |||||x  <br/> |
|CompleteDate  <br/> |||||x  <br/> |
|Completename  <br/> ||x  <br/> ||||
|Conferencetype  <br/> |x  <br/> |||||
|ConflictingMeetingCount  <br/> |x  <br/> |||||
|ConflictingMeetings  <br/> |x  <br/> |||||
|Kontakte  <br/> |||||x  <br/> |
|ContactSource  <br/> ||x  <br/> ||||
|ConversationId  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ConversationIndex  <br/> |||x  <br/> |x  <br/> ||
|ConversationTopic  <br/> |||x  <br/> |x  <br/> ||
|Kultur  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DateTimeCreated  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DateTimeReceived  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DateTimeSent  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DateTimeStamp  <br/> |x  <br/> |||||
|DelegationState  <br/> |||||x  <br/> |
|Delegator  <br/> |||||x  <br/> |
|DeletedOccurrences  <br/> |x  <br/> |||||
|Abteilung  <br/> ||x  <br/> ||||
|Verzeichnis-Nr  <br/> ||x  <br/> ||||
|DirectReports  <br/> ||x  <br/> ||||
|DisplayCc  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DisplayName  <br/> ||x  <br/> ||||
|Displayto ursprünglicher  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
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
|Erzeugung  <br/> ||x  <br/> ||||
|GivenName  <br/> ||x  <br/> ||||
|HasAttachments  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|HasPicture  <br/> ||x  <br/> ||||
|Imaddresses  <br/> ||x  <br/> ||||
|Importance  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|Initialen  <br/> ||x  <br/> ||||
|InReplyTo  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|InternetMessageId  <br/> |||x  <br/> |x  <br/> ||
|InternetMessageHeaders  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsAllDayEvent  <br/> |x  <br/> |||||
|Isassociated  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsCancelled  <br/> |x  <br/> |||||
|IsComplete  <br/> |||||x  <br/> |
|IsDeliveryReceiptRequested  <br/> |||x  <br/> |||
|IsDraft  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|Isfromme  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|Ismeeting  <br/> |x  <br/> |||||
|IsOnlineMeeting  <br/> |x  <br/> |||||
|IsRead  <br/> |||x  <br/> |||
|IsReadReceiptRequested  <br/> |||x  <br/> |||
|IsRecurring  <br/> |x  <br/> ||||x  <br/> |
|IsResend  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsResponseRequested  <br/> |x  <br/> ||x  <br/> |||
|Issubmitted  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|IsUnmodified  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ItemClass  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|Itemid  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|JobTitle  <br/> ||x  <br/> ||||
|LastModifiedName  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|LastModifiedTime  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|LastOccurrance  <br/> |x  <br/> |||||
|LegacyFreeBusyStatus  <br/> |x  <br/> |||||
|Standort  <br/> |x  <br/> |||||
|Manager  <br/> ||x  <br/> ||||
|MeetingRequestWasSent  <br/> |x  <br/> |||||
|MeetingTimeZone  <br/> |x  <br/> |||||
|MeetingWorkspaceUrl  <br/> |x  <br/> |||||
|MiddleName  <br/> ||x  <br/> ||||
|Reisekilometer  <br/> ||x  <br/> |||x  <br/> |
|ModifiedOccurrances  <br/> |x  <br/> |||||
|Myresponsetype  <br/> |x  <br/> |||||
|NetShowUrl  <br/> |x  <br/> |||||
|NickName  <br/> ||x  <br/> ||||
|Notes  <br/> ||x  <br/> ||||
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
|Gebucht  <br/> ||||x  <br/> ||
|Beruf  <br/> ||x  <br/> ||||
|ReceivedBy  <br/> |||x  <br/> |||
|ReceivedRepresenting  <br/> |||x  <br/> |||
|Reccurrence  <br/> |x  <br/> ||||x  <br/> |
|Verweise  <br/> |||x  <br/> |x  <br/> ||
|ReminderDueBy  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ReminderIsSet  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ReminderMinutesBeforeStart  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ReplyTo  <br/> |||x  <br/> |||
|RequiredAttendees  <br/> |x  <br/> |||||
|Ressourcen  <br/> |x  <br/> |||||
|ResponseObjects  <br/> |x (1)  <br/> |x (1)  <br/> |x (1)  <br/> |x (1)  <br/> |x (1)  <br/> |
|Absender  <br/> |||x  <br/> |x  <br/> ||
|Vertraulichkeit  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|Größe  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|Ehepartnername  <br/> ||x  <br/> ||||
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
  
1. Enthalten beim [binden an ein Element](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) und in der Antwort des [GetItem-Vorgangs](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx). Nicht im Ergebnis der [Item. FindItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) -Methode oder der Antwort des [FindItem-Vorgangs](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)enthalten.
    
## <a name="see-also"></a>Siehe auch

- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [FindItem-Vorgang](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
- [GetItem-Vorgang](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)
    
- [FindFolder Operation](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [GetFolder Operation](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)
    

