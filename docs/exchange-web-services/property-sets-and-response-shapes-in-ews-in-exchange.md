---
title: Eigenschaftensätze und Antwort shapes in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 04a29804-6067-48e7-9f5c-534e253a230e
description: Erfahren Sie mehr über die Antwort Shapes verwalten und Eigenschaftensätze, die durch die EWS zurückgegeben werden managed API und die EWS in Exchange.
ms.openlocfilehash: d9fd6c155438dfd03cfc9536397316cf3faa2287
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757141"
---
# <a name="property-sets-and-response-shapes-in-ews-in-exchange"></a>Eigenschaftensätze und Antwort shapes in EWS in Exchange

Erfahren Sie mehr über die Antwort Shapes verwalten und Eigenschaftensätze, die durch die EWS zurückgegeben werden managed API und die EWS in Exchange.
  
Der Exchange-Datenspeicher bietet eine flexible Storage-Lösung, mit die Sie andere Elemente, wie Kontakte und Kalendereinträge im selben Ordner speichern kann. jedoch es kann erschweren die Daten zu verwalten, die von einem Aufruf von EWS-Vorgang zurückgegeben wird, oder ein EWS managed-API-Methode.
  
Um die Daten zu verwalten, die von Exchange Online, Exchange Online als Teil von Office 365-Version oder Excahange zurückgegeben wird, beginnend mit Exchange 2013 erleichtern die EWS Managed API verwendet Eigenschaftensätze und EWS Antwort Shapes. Dies sind die vordefinierten Sammlungen, die am häufigsten verwendeten Eigenschaften eines Elements Store bereitstellen. Die Gruppe von Eigenschaften, die zurückgegeben wird, wird durch den Elementtyp bestimmt. Das bedeutet, dass beim Binden eines Elements mithilfe der Exchange Managed API [Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) -Methode können Sie eine andere Menge von Eigenschaften je nach den Typ des Elements an den Sie binden erhalten. Bindung an ein Kalenderelement gibt eine andere Menge von Eigenschaften als Bindung zu einem Kontaktelement zurück. Bei Verwendung von EWS gibt den [GetItem Operation](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) ebenso eine andere Menge von Eigenschaften basierend auf den Typ des Elements, das zurückgegeben wird. 
  
Binden an einen Ordner mit der [Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) -Methode oder mithilfe der [GetFolder-Vorgang](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) gibt auch verschiedene Sätze von Eigenschaften basierend auf den Ordner, den Sie anfordern. 
  
**In Tabelle 1. Vordefinierte Antwort shapes**

|**Antwort-shape**|**EWS Managed-API-Entsprechung**|**Beschreibung**|
|:-----|:-----|:-----|
|Nur-ID  <br/> |[BasePropertySet.IdOnly](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) <br/> |Gibt nur den Bezeichner des Elements oder Ordners zurück. Die meisten sollte verwenden Sie dieses Shape Antwort, und geben Sie alle zusätzlichen Eigenschaften, die erforderlich sind.  <br/> |
|Standard  <br/> |–  <br/> |Gibt eine vordefinierte Reihe von Eigenschaften, die den Standardwert für das Element oder einen Ordner (nur EWS) sind.  <br/> |
|Alle Eigenschaften  <br/> |[BasePropertySet.FirstClassProperties](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) <br/> |Die Eigenschaften, die am häufigsten Clientanwendungen verwendeten zurückgegeben. Sie können zusätzliche Eigenschaften mithilfe eines Pfads Eigenschaft zurückgeben.  <br/> |
   
## <a name="default-response-shapes"></a>Standard-Antwort-shapes

EWS enthält eine Reihe von Shapes des Standard-Antwort für Ordner und Elemente. 
  
Die folgende Tabelle enthält die Standardeigenschaften, die durch die [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) und [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) EWS-Vorgänge für jeden Ordner zurückgegeben werden. 
  
**In Tabelle 2. Eigenschaften von Ordnern**

|**Eigenschaft**|**Posteingang**|**Kalender**|**Kontakte**|**Gelöschte Elemente**|**Entwürfe**|**Anmerkungen**|**Andere Ordner**|**Postausgang**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Anzeigename  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Ordner-ID  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Anzahl der Unterordner  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Gesamtzahl  <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Ungelesene Nachrichten  <br/> |X  <br/> |||X  <br/> |X  <br/> ||X  <br/> |X  <br/> |
   
Die folgende Tabelle enthält die Standardeigenschaften, die durch die [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) und [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) -EWS-Vorgänge für die einzelnen Element zurückgegeben werden. 
  
**Tabelle 3. Standard-Eigenschaften**

|**Eigenschaft**|**Kalenderelement**|**Kontaktelement**|**Nachrichten-Element**|**Aufgabenelement**|
|:-----|:-----|:-----|:-----|:-----|
|Textkörper  <br/> |||X(1)  <br/> ||
|CalendarItemType  <br/> ||x  <br/> |||
|CompanyName  <br/> ||x  <br/> |||
|CompleteName  <br/> ||x  <br/> |||
|"Datetimecreated"  <br/> |||x  <br/> ||
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
|Speicherort  <br/> |x  <br/> ||||
|Organisator  <br/> |x  <br/> ||||
|PercentComplete  <br/> ||||x  <br/> |
|PhoneNumbers  <br/> ||x  <br/> |||
|PhysicalAddresses  <br/> ||x  <br/> |||
|ResponseObjects  <br/> |x(1)  <br/> ||x(1)  <br/> ||
|Sensitity  <br/> |||x  <br/> ||
|Größe  <br/> |||x  <br/> ||
|StartDate  <br/> ||||x(2)  <br/> |
|Status  <br/> ||||x  <br/> |
|Subject  <br/> |x  <br/> ||x  <br/> |x  <br/> |
   
Hinweise:
  
1. In der Antwort aus der **GetItem** Operation enthalten. In der Antwort vom **FindItem** -Vorgang enthalten nicht. 
    
2. Nur enthalten in der Antwort, wenn das Feld Daten enthält. Nicht enthalten in der Antwort, wenn das Feld leer ist.
    
### <a name="all-properties-set-and-response-shape"></a>Alle Eigenschaften festlegen und Antwort-shape

Die folgende Tabelle enthält die erstklassigen Eigenschaften, die durch Aufrufen der EWS Managed API [Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) und [Item.FindItems](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) EWS Managed API-Methoden und "alle Eigenschaften" Antwort Form zurückgegeben, die durch die [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) und [zurückgegeben werden GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) EWS-Vorgänge. 
  
Sie können zusätzliche Eigenschaften der-Eigenschaft festzulegen oder erweiterte Eigenschaften einbeziehen hinzufügen. Weitere Informationen hierzu finden Sie unter [Eigenschaften und erweiterten Eigenschaften in EWS in Exchange](properties-and-extended-properties-in-ews-in-exchange.md).
  
**In Tabelle 4. Erstklassige Eigenschaften**

|||||||
|:-----|:-----|:-----|:-----|:-----|:-----|
|Eigenschaft  <br/> |Kalenderelement  <br/> |Kontaktelement  <br/> |Nachrichten-Element  <br/> |POST-Element  <br/> |Aufgabenelement  <br/> |
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
|Textkörper  <br/> |x(1)  <br/> |x(1)  <br/> |x(1)  <br/> ||x(1)  <br/> |
|BusinessHomePage  <br/> ||x  <br/> |x  <br/> |||
|CalendarItemType  <br/> |x  <br/> |||||
|Kategorien  <br/> |x  <br/> ||x  <br/> |x  <br/> |x  <br/> |
|CcRecipients  <br/> |||x  <br/> |||
|ChangeCount  <br/> |||||x  <br/> |
|Untergeordnete Objekte  <br/> ||x  <br/> ||||
|Companies  <br/> |||||x  <br/> |
|"CompleteDate" darf  <br/> |||||x  <br/> |
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
|"Datetimecreated"  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DateTimeReceived  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DateTimeSent  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DateTimeStamp  <br/> |x  <br/> |||||
|DelegationState  <br/> |||||x  <br/> |
|Delegator  <br/> |||||x  <br/> |
|DeletedOccurances  <br/> |x  <br/> |||||
|Abteilung  <br/> ||x  <br/> ||||
|DirectoryId  <br/> ||x  <br/> ||||
|DirectReports  <br/> ||x  <br/> ||||
|DisplayCc  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DisplayName  <br/> ||x  <br/> ||||
|DisplayTo  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|DueDate  <br/> |||||x  <br/> |
|Duration  <br/> |x  <br/> |||||
|EffectiveRights  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|EmailAddresses  <br/> ||x  <br/> ||||
|Ende  <br/> |x  <br/> |||||
|EndTimeZone  <br/> |x  <br/> |||||
|FileAs  <br/> ||x  <br/> ||||
|FileAsMapping  <br/> ||x  <br/> ||||
|FirstOccurance  <br/> |x  <br/> |||||
|Von  <br/> |||x  <br/> |x  <br/> ||
|Generierung  <br/> ||x  <br/> ||||
|Vorname  <br/> ||x  <br/> ||||
|HasAttachments  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|HasPicture  <br/> ||x  <br/> ||||
|ImAddresses  <br/> ||x  <br/> ||||
|Wichtigkeit  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
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
|ZuletztGeändertUm  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|LastOccurrance  <br/> |x  <br/> |||||
|LegacyFreeBusyStatus  <br/> |x  <br/> |||||
|Speicherort  <br/> |x  <br/> |||||
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
|Anmerkungen  <br/> ||x  <br/> ||||
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
|Ereignisserie  <br/> |x  <br/> ||||x  <br/> |
|Referenzen  <br/> |||x  <br/> |x  <br/> ||
|ReminderDueBy  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ReminderIsSet  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ReminderMinutesBeforeStart  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|ReplyTo  <br/> |||x  <br/> |||
|RequiredAttendees  <br/> |x  <br/> |||||
|Ressourcen  <br/> |x  <br/> |||||
|ResponseObjects  <br/> |x(1)  <br/> |x(1)  <br/> |x(1)  <br/> |x(1)  <br/> |x(1)  <br/> |
|Absender  <br/> |||x  <br/> |x  <br/> ||
|Vertraulichkeit  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|Größe  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|SpouseName  <br/> ||x  <br/> ||||
|Beginn  <br/> |x  <br/> |||||
|StartDate  <br/> |||||x  <br/> |
|StartTimeZone-Zeitzone  <br/> |x  <br/> |||||
|Status  <br/> |||||x  <br/> |
|StatusDescription  <br/> |||||x  <br/> |
|Subject  <br/> |x  <br/> |x  <br/> |x  <br/> ||x  <br/> |
|Nachname  <br/> ||x  <br/> ||||
|TimeZone  <br/> |x  <br/> |||||
|ToRecipients  <br/> |||x  <br/> |||
|TotalWork  <br/> |||||x  <br/> |
|WebClientEditFormQueryString  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
|WebClientReadFormQueryString  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |x  <br/> |
   
Hinweise:
  
1. Wann enthalten [Bindung zu einem Element](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) und in der Antwort vom [GetItem Operation](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx). Nicht enthalten in das Ergebnis der [Item.FindItems](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) -Methode oder der Antwort vom [FindItem Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx).
    
## <a name="see-also"></a>Siehe auch

- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [FindItem-Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
- [GetItem Operation](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)
    
- [FindFolder Operation](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [GetFolder Operation](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)
    

