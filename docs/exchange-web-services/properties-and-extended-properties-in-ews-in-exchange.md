---
title: Eigenschaften und erweiterte Eigenschaften in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 68623048-060e-4602-b3fa-62617a94cf72
description: Informationen zum Definieren von und Zugreifen auf Eigenschaften von Elementen und Ordnern mit EWS in Exchange.
ms.openlocfilehash: 0c01d9bd21cbef0a3536c8dbd85e192199b7b8ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757124"
---
# <a name="properties-and-extended-properties-in-ews-in-exchange"></a>Eigenschaften und erweiterte Eigenschaften in EWS in Exchange

Informationen zum Definieren von und Zugreifen auf Eigenschaften von Elementen und Ordnern mit EWS in Exchange.
  
Ein Exchange-Postfach enthält eine große Anzahl von Elementen, einschließlich e-Mail-Nachrichten, Terminen, Besprechungen und So weiter. Diese Elemente bestehen aus Eigenschaften; die Eigenschaften werden die Elemente beschrieben. Elementeigenschaften können Sie eine [Suche](search-and-ews-in-exchange.md), [Synchronisieren von Änderungen an Listenelementen](mailbox-synchronization-and-ews-in-exchange.md)und [Erstellen von benutzerdefinierten Eigenschaftentypen](http://code.msdn.microsoft.com/exchange/Exchange-2013-Create-314db25a)ausführen. Dieser Artikel enthält eine Übersicht über die Eigenschaften und wie Sie mit den Eigenschaften in der Anwendung arbeiten können.
  
## <a name="exchange-item-properties"></a>Exchange-Elementeigenschaften
<a name="ItemsAreProperties"> </a>

Elemente und Ordner in Exchange sind im Wesentlichen Tabellenzeilen. Die Haupt-Eigenschaft eines Elements oder Ordners identifiziert ist des [EWS-Bezeichner](ews-identifiers-in-exchange.md). Zwar in der Exchange-Datenbank für EWS andere Bezeichner-bezogene Eigenschaften sind, fungiert der EWS-Bezeichner als Primärschlüssel für die Auflistung von Eigenschaften, die ein Element zu beschreiben. Die EWS-Bezeichner-Eigenschaft besteht aus zwei Teilen:
  
- Eine [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) oder [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) -Eigenschaft, die das Element identifiziert. 
    
- Eine **ChangeKey** -Eigenschaft, die enthält Statusinformationen zu gibt an, ob eines Elements oder Ordners geändert hat 
    
Alle Elemente in einem Postfach in der gleichen Exchange-Datenbank gespeichert sind, und verwenden Sie dasselbe Datenbankschema. Elemente werden durch eine Kombination unterschieden Speichern von der Eigenschaft ["itemclass"](http://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) -Eigenschaft Einschränkungen und die Ebenen der Business-Logik, die beeinflussen, wie sie in der Exchange verwaltet werden. Tabelle 1 zeigt, wie Eigenschaften über verschiedene Elementtypen angewendet werden. In diesem Beispiel, e-Mail und Termine Elemente. Beide Elemente müssen einen Wert für die [Subject](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) -Eigenschaft. Aber beachten Sie, dass die [IsAllDayEvent](http://msdn.microsoft.com/library/29140a64-9d7a-4a14-a10d-c98197c9831b%28Office.15%29.aspx) -Eigenschaft für das e-Mail-Element nicht festgelegt wurde, und die **IsReadReceiptRequested** -Eigenschaft ist nicht für den Termin festgelegt. Zum Glück müssen Sie nicht wissen, welche Eigenschaften für jede Elementklasse gelten. EWS behandelt dies für Sie. 
  
**In Tabelle 1. Vergleich der Termin und e-Mail-Eigenschaften**

|**Elementtyp**|**Item-Klasse**|**Betreff**|**IsAllDayEvent**|**IsReadReceiptRequested**|
|:-----|:-----|:-----|:-----|:-----|
|E-Mail  <br/> |IPM.Note  <br/> |Statusbericht: Projekt X abgeschlossen  <br/> |NULL  <br/> |true  <br/> |
|Termin  <br/> |IPM.Appointment  <br/> |Contoso-Unternehmenssitzung  <br/> |False  <br/> |NULL  <br/> |
   
Das EWS-Schema unterstützt viele der von der Exchange-Datenbank verwalteten Einschränkungen und der Geschäftslogikschichten zwischen EWS und der Exchange-Datenbank. Das EWS-Schema wendet ein definiertes Set von Eigenschaften auf jeden Elementtyp an. Im folgenden werden die stark typisierten. von EWS bereitgestellten Exchange-Datenbankelemente aufgeführt:  
  
- E-Mails
    
- Termine
    
- Kontakte
    
- Verteilerlisten
    
- Besprechungsnachrichten
    
- Besprechungsanfragen
    
- Besprechungsantworten
    
- Besprechungsabsagen
    
- Aufgaben
    
- Bereitstellungselemente
    
Generische Elemente werden von EWS als E-Mails zurückgegeben. Die EWS Managed API implementiert alle diese Elementtypen.
  
> [!NOTE]
> Antwortobjekte werden nur vom Client an den Server als Antwort auf die von anderen Personen empfangenen Elemente gesendet. Sie sind nicht in der Exchange-Datenbank vorhanden. 
  
## <a name="what-are-properties-in-ews"></a>Was sind Eigenschaften in EWS?
<a name="WhatAreEWSProperties"> </a>

Das EWS-Schema beschreibt die Daten, die zwischen einem Client EWS und Exchange gesendet wird. Ein großer Teil des Schemas beschreibt die Element- und Eigenschaften, die Sie in der Exchange-Datenbank zugreifen können. Das EWS-Schema beschreibt die XML-Darstellung der Exchange-Datenbankeigenschaften, die für Ihre Anwendung verfügbar sind. Die tatsächlichen Eigenschaften, die im Hinblick auf die Eigenschaften verfügbar sind, was bilden diese anfordern und übernehmen und die Werte, die sie zurückgeben, variieren, je nachdem was Sie tun möchten. Beispielsweise die **Body** -Eigenschaft gibt nur die ersten 512 Zeichen in einem Vorgang **FindItem** zurück, aber die **GetItem** Operation gibt den vollständigen Text des Elements zurück. Obwohl die meisten Eigenschaften festgelegt werden und abrufbar sind, werden einige Eigenschaften nur von Exchange festgelegt. Jede Eigenschaft vorhanden ist im Schema in einem XML-Format, entweder die-Eigenschaft entspricht, wie es in der Exchange-Datenbank gespeichert ist, oder von Eigenschaften in der Exchange-Datenbank gespeicherten berechnet wird. Die **Subject** -Eigenschaft ist ein Beispiel für eine Eigenschaft festgelegt werden kann. die **UnreadCount** -Eigenschaft für einen Ordner ist ein Beispiel für eine berechnete Eigenschaft. Eine Kerngruppe von Eigenschaften gelten für die Elementtypen Core zur Verfügung. 
  
Die folgenden Faktoren bestimmen die festgelegte Eigenschaft, die Ihre Anwendung von Exchange abruft:  
  
- Der Vorgang, den die Anwendung aufruft
    
- Das Basisshape der Antwort
    
- Der Elementtyp
    
- Die angegebenen Eigenschaftspfade
    
Es ist wichtig zu verstehen, wie diese verschiedenen Faktoren Einfluss auf die Daten, die Sie zugreifen können. Als mit dem Beispiel für die **Body** -Eigenschaft, die weiter oben erwähnten sind einige Informationen abhängig von verschiedenen Faktoren bedingt verfügbar. Grundlegendes zu diesen Faktoren mithilfe eines Problems Zeit sparen möglicherweise wählen Sie die richtigen Optionen auf Informationen zugreifen, werden soll. Um zu ermitteln, welche Eigenschaften zugegriffen werden kann, müssen Sie diese Faktoren bestimmen, wie Sie die Eigenschaften zugreifen, um zu testen Ihrer Anwendung benötigt. In diesem Abschnitt wird beschrieben, wie diese verschiedenen Faktoren beeinflussen in EWS Antworten welche Eigenschaften zurückgegeben werden. 
  
### <a name="ews-response-shapes"></a>EWS-Antwortshapes

Exchange speichert eine Vielzahl von Informationen zu Elementen. In manchen Fällen die Anwendung nicht alle Informationen benötigen, und in vielen Fällen ist es am besten nicht alle darauf zuzugreifen. [EWS-Antwort-Shapes](property-sets-and-response-shapes-in-ews-in-exchange.md), auch als bezeichnet Eigenschaft Shapes, geben Sie an, welche Eigenschaften vom Server zurückgegeben werden. Die Hauptkomponente von der Antwort-Shape ist die Basis-Form. Eine base Form handelt es sich um einen vordefinierten Standard-Eigenschaftenbehälter für stark typisierten Elemente. EWS Managed API entspricht die Basis Form der [BasePropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx). EWS enthält drei Standard-Antwort-Shapes.
  
**In Tabelle 2. Standard-Antwort-shapes**

|**Standard-Antwort Shape-name**|**EWS Managed-API-Entsprechung**|**Beschreibung**|
|:-----|:-----|:-----|
|IdOnly  <br/> |BasePropertySet.IdOnly-Wert  <br/> |Nur die EWS-Bezeichner und Key ändern, werden zurückgegeben. Wenn der Client verwendet zurückgegeben Sie alle Eigenschaften, das AllProperties oder Standard-Shape, verwenden Sie das IdOnly-Shape, und geben Sie zusätzliche Eigenschaften mithilfe des Eigenschaftenpfads für die **PropertySet** -Klasse festlegen. Die meisten sollten die IdOnly Antwort Form mit zusätzlichen Eigenschaften angegeben verwenden. Dadurch wird die Menge der nicht verwendeten Daten, die von Clients angefordert werden.  <br/> |
|Standard  <br/> |–  <br/> |Eine Gruppe von Standardeigenschaften für den Elementtyp. Verwenden Sie dieses Antwortshape nur. wenn Ihre Anwendung alle Eigenschaften verwendet.    <br/> |
|AllProperties  <br/> |BasePropertySet.FirstClassProperties-Wert  <br/> |Eine größere Gruppe von Eigenschaften als das Standardshape. Auch wenn der Name dies andeutet, gibt diese Option nicht alle Eigenschaften eines Elements zurück. Dieser Eigenschaftensatz gibt die Eigenschaften zurück, die am häufigsten von Clientanwendungen verwendeten werden. Wenn Sie weitere Eigenschaften benötigen, können Sie diese durch den entsprechenden Eigenschaftspfad anfordern.   <br/> Wenn die Anwendung nicht alle Eigenschaften zurückgegeben, die mit diesem Shape Antwort verwendet, verwenden Sie IdOnly Antwort Form mit zusätzlichen Eigenschaften angegeben.  <br/> |
   
Viele EWS-Vorgänge geben Elemente und die zugehörigen Eigenschaften zurück. Unabhängig vom angegebenen Antwortshape, können unterschiedliche Vorgänge unterschiedliche Eigenschaftensätze zurückgeben. Unterschiedliche Elementtypen geben je nach Vorgang und festgelegtem Antwortshape unterschiedliche Eigenschaften zurück. Die folgenden Vorgänge verwenden Antwortshapes, um die zurückzugebenden Eigenschaften zu identifizieren.
  
**Tabelle 3. Vorgänge, die Antwort-Shapes verwenden**

|**EWS-Vorgang**|**EWS Managed API-Methode**|
|:-----|:-----|
|[GetConversationItems](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) <br/> |[ExchangeService.GetConversationItems-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) <br/> |
|[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |[Folder.Bind-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> |
|[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |[Item.Bind-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [ExchangeService.BindToItems-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) <br/> |
|[FindConversation](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) <br/> |[ExchangeService.FindConversation-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findconversation%28v=exchg.80%29.aspx) <br/> |
|[FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |[Folder.FindFolders-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService.FindFolders-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) <br/> |
|[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |[Folder.FindItems-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> [ExchangeService.FindItems-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |
|[FindPeople](http://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) <br/> |Nicht implementiert.  <br/> |
|[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) <br/> |[ExchangeService.ResolveNames-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) <br/> |
|[SearchMailboxes](http://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |[ExchangeService.SearchMailboxes-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.searchmailboxes%28v=exchg.80%29.aspx) <br/> [ExchangeService.BeginSearchMailboxes-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.beginsearchmailboxes%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) <br/> |[ExchangeService.SyncFolderHierarchy-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) <br/> |[ExchangeService.SyncFolderItems-Methode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) <br/> |
   
Eigenschaftshapes stellen eine elementare Methode dar, um die Eigenschaften zu identifizieren, die Ihre Anwendung zurückgeben soll. In manchen Fällen benötigt Ihre Anwendung jedoch einen begrenzten Satz bestimmter Eigenschaften. Zu diesem Zweck können Sie den Eigenschaftspfad verwenden.
  
### <a name="choose-properties-by-their-property-path"></a>Wählen von Eigenschaften anhand des entsprechenden Eigenschaftspfads

Bei einem EWS-Eigenschaftspfad handelt es sich um Metadaten, die zum Identifizieren von Eigenschaften in einer Anforderung oder Antwort verwendet werden.  
  
**In Tabelle 4. Pfad Eigenschaftentypen**

|**Pfad Eigenschaftentyp**|**Schematyp**|**EWS Managed API-Implementierung**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
|FieldUri  <br/> |PathToUnindexedFieldType  <br/> |Typen, die von [ServiceObjectSchema](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceobjectschema%28v=exchg.80%29.aspx)erben.  <br/> |Der am häufigsten verwendeten Eigenschaftenpfad. FieldUri-Eigenschaftenpfade werden auf ein **PropertySet** -Objekt in die EWS Managed API angegeben. Die meisten EWS-Eigenschaften können durch den Pfad der FieldUri-Eigenschaft angegeben werden. Dies wird durch die UnindexedFieldURIType im EWS-Schema beschrieben.  <br/> Der XML-Code des FieldUri-Eigenschaftspfad sieht wie folgt aus:  <br/> ```XML<FieldURI FieldURI="item:Subject"/>```Diese Eigenschaft Path entspricht dem ItemSchema.Subject in die EWS Managed API.  <br/> |
|IndexedFieldUri  <br/> |PathToIndexedFieldType  <br/> |Typen, die von [ItemSchema](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemschema%28v=exchg.80%29.aspx)erben.  <br/> |Wörterbuch-Eigenschaften, die einen Index-Eigenschaft zum Angeben des zurückzugebende Werts erfordern identifiziert. Verwenden Sie diesen Pfad, wenn eine Eigenschaft mehr als einen Wert enthalten kann. Dies wird durch die **DictionaryURIType** -Eigenschaft im EWS-Schema beschrieben. **DictionaryURIType** -Eigenschaftenpfade werden auf ein **PropertySet** -Objekt in die EWS Managed API angegeben.  <br/> Der XML-Code des IndexedFieldUri-Eigenschaftspfad sieht wie folgt aus:  <br/> ```XML<IndexedFieldURI FieldURI="contacts:PhysicalAddress:Street FieldIndex="Home"/>```|
|ExtendedFieldUri  <br/> |PathToExtendedFieldType  <br/> |[ExtendedPropertyDefinition](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) <br/> |Gibt eine erweiterte Eigenschaftsdefinition an, die benutzerdefinierte oder nicht schematisierte Eigenschaften von Elementen identifiziert.  <br/> Der XML-Code des ExtendedFieldUri-Eigenschaftspfad sieht wie folgt aus:  <br/> ```XML<ExtendedFieldURI> PropertyTag="0x1234" PropertyType="Integer" />```|
|ExceptionFieldUri  <br/> |ExceptionFieldURI  <br/> |[ServiceResponse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) <br/> |Gibt die Eigenschaften, die einen Fehler in einer Antwort EWS zugeordnet sind. Dies wird durch den **ExceptionPropertyURIType** Typ im EWS-Schema beschrieben. Dies tritt nur im **MessageXml** -Element des Fehlerantworten, die bei der Arbeit mit Kalender Serienmuster auftreten.  <br/> |
   
Es empfiehlt sich Wenn Sie Eigenschaften anfordern, verwenden Sie das IdOnly base Shape ([BasePropertySet.IdOnly](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) in die EWS Managed API) und fordern Sie dann nur die Eigenschaften, die die Anwendung benötigt, durch die Eigenschaftenpfade angeben. 
  
### <a name="schematized-properties"></a>Schematisierte Eigenschaften

Die meisten Eigenschaften, die Ihre EWS-Client muss werden von der EWS-Schema beschrieben. Die primären Ordner und Definitionen, die die Eigenschaftendefinitionen enthalten, werden im Schema types.xsd gefunden. Die folgenden Typen von Schema enthalten die Eigenschaftendefinitionen für die meisten Objekte, die Sie verwenden können.
  
**Tabelle 5. Schematypen, die Definitionen enthalten**

|**Typ der EWS-schema**|**EWS Managed API Typ entspricht**|**Definiert die...**|
|:-----|:-----|:-----|
|**ItemType** <br/> |[Item-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den Basiselementtyp. Dieser Typ kann von einem Client erstellt werden, wird jedoch nie von Exchange zurückgegeben. Exchange gibt ein MessageType-Objekt für alle generische Objekte zurück.  <br/> |
|**MessageType** <br/> |[Klasse "EmailMessage"](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für das E-Mail-Objekt und alle generischen Objekte.  <br/> |
|**CalendarItemType** <br/> |[Termin-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den Kalenderelementtyp. Dies umfasst einzelne und wiederkehrende Termine.  <br/> |
|**ContactItemType** <br/> |[Wenden Sie sich an Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für das Kontaktelement.  <br/> |
|**DistributionListType** <br/> |[ContactGroup-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für die persönliche Verteilerliste.  <br/> |
|**MeetingMessageType** <br/> |[MeetingMessage-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingmessage%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den Besprechungsnachrichttyp.  <br/> |
|**MeetingRequestMessageType** <br/> |[MeetingRequest-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingrequest%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den Besprechungsanfragentyp.  <br/> |
|**MeetingResponseMessageType** <br/> |[MeetingResponse-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingresponse%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den Besprechungsantworttyp.  <br/> |
|**MeetingCancellationMessageType** <br/> |[MeetingCancellation-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingcancellation%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den Besprechungsabsagentyp.  <br/> |
|**TaskType** <br/> |[Task-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den Aufgabentyp.  <br/> |
|**PostItemType** <br/> |[PostItem-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.postitem%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den Bereitstellungselementtyp.  <br/> |
|**FolderType** <br/> |[Ordner-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den Ordnertyp.  <br/> |
|**CalendarFolderType** <br/> |[CalendarFolder-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den SearchFolder-Typ.  <br/> |
|**ContactsFolderType** <br/> |[ContactsFolder-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den ContactsFolder-Typ.  <br/> |
|**SearchFolderType** <br/> |["SearchFolder"-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den SearchFolder-Typ.  <br/> |
|**TasksFolderType** <br/> |[TasksFolder-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den TaskFolder-Typ.  <br/> |
|**UserConfigurationType** <br/> |[UserConfiguration-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den UserConfiguration-Typ.  <br/> |
   
Während die Eigenschaften im EWS-Schema für viele Clientanwendungen ausreichend sind, können Sie einige Szenarien mithilfe von nur was im Schema beschrieben ist nicht implementieren. Für diese Szenarien können Sie erweiterte Eigenschaften. 
  
### <a name="extended-properties-aka-non-schematized-properties"></a>Erweiterte Eigenschaften (auch nicht schematisierte Eigenschaften genannt)

Mit erweiterten Eigenschaften können Sie benutzerdefinierte Eigenschaften erstellen, mit denen Sie auf Elemente und Ordner im Exchange-Speicher zugreifen können, die nicht im EWS-Schema definiert sind. Sie können sie zum Zugreifen auf die Eigenschaften des systemeigenen MAPI-Elements und Ordnereigenschaften in der Exchange-Datenbank verwenden. Mit erweiterten Eigenschaften ist der Zugriff auf alle schematisierten Eigenschaften möglich, da diese schematisierten Eigenschaften nichts Anderes als MAPI-Eigenschaften in der Exchange-Datenbank sind.  
  
PathToExtendedFieldType Schema-Typ, befindet sich im types.xsd-Schema definiert den XML-Code, die eine erweiterte Eigenschaft darstellt. Dieses Schematyps definiert das [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) -Element im XML-Instanzen. Anders ausgedrückt, definiert den XML-Code, die zwischen dem Dienst und dem Client gesendet wird. Der Typ des ExtendedPropertyType Schema definiert sowohl das [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) -Element und den Wert oder Array von Werten, die eine erweiterte Eigenschaft enthält. Die folgende Tabelle enthält die ungefähre der erweiterten Eigenschaft XML-Zuordnung und Implementierung für Elemente in die EWS Managed API. 
  
**Tabelle 6. Erweiterte Eigenschaft XML gemäß der Implementierung in die EWS Managed API**

|**EWS Managed API-Implementierung**|**Was er enthält**|**Was es zugeordnet ist**|
|:-----|:-----|:-----|
|[Item.ExtendedProperties-Eigenschaft](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.extendedproperties%28v=exchg.80%29.aspx) <br/> |Eine Sammlung erweiterter Eigenschaften eines Elements.  <br/> |Wird einer oder mehreren Instanzen von erweiterten Eigenschaften eines Elements zugeordnet.  <br/> |
|[ExtendedProperty-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.extendedproperty%28v=exchg.80%29.aspx) <br/> |Die Definition und Werte der erweiterten Eigenschaft.  <br/> |Wird dem ExtendedPropertyType-Schematyp zugeordnet.  <br/> |
|[ExtendedPropertyDefinition-Klasse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) <br/> |Die Definition einer erweiterten Eigenschaft.  <br/> |Wird dem PathToExtendedFieldType-Schematyp zugeordnet.  <br/> |
   
Weitere Informationen zum Verwenden erweiterter Eigenschaften in Ihrer Anwendung finden Sie in den folgenden Codebeispielen:  
  
- [MFCMAPI (engl.)](http://mfcmapi.codeplex.com/)
    
- [Exchange 2013: Programmgesteuertes Bereitstellen von benutzerdefinierten X-Headern](http://code.msdn.microsoft.com/exchange/Exchange-2013-Provision-d4ef5719)
    
- [Exchange 2013: Greifen Sie eine Eigenschaft zu, indem Sie die Eigenschaftentag](http://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-719875ac)
    
- [Exchange 2013: Zugriff auf eine benannte Eigenschaft anhand des Bezeichners](http://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-02dbe22f)
    
- [Exchange 2013: Greifen Sie eine benannte Eigenschaft zu, indem Sie deren Namen](http://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-6556e183)
    
- [Exchange 2013: Zugreifen Sie auf eine-Eigenschaft von Eigenschaftensatz-GUID und Namen](http://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-4021f971)
    
- [Exchange 2013: Erstellen von benutzerdefinierten programmgesteuert erweiterte Eigenschaften](http://code.msdn.microsoft.com/exchange/Exchange-2013-Create-314db25a)
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_inthissection"> </a>

- [Bestimmung X-Header im Exchange mithilfe der Exchange-Webdienste](how-to-provision-x-headers-by-using-ews-in-exchange.md)
    
- [EWS-Eigenschaft-bezogene Fehler](ews-property-related-errors.md)
    
## <a name="see-also"></a>Siehe auch


- [Erste Schritte mit Webdiensten in Exchange](start-using-web-services-in-exchange.md)
    
- [MFCMAPI (engl.)](http://mfcmapi.codeplex.com/)
    

