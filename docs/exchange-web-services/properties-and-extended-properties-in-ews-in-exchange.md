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
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757124"
---
# <a name="properties-and-extended-properties-in-ews-in-exchange"></a>Eigenschaften und erweiterte Eigenschaften in EWS in Exchange

Informationen zum Definieren von und Zugreifen auf Eigenschaften von Elementen und Ordnern mit EWS in Exchange.
  
Ein Exchange-Postfach enthält eine große Anzahl von Elementen, einschließlich E-Mails, Terminen, Besprechungen usw. Diese Elemente bestehen aus Eigenschaften; die Eigenschaften beschreiben die Elemente. Sie können Elementeigenschaften zum Ausführen einer [Suche](search-and-ews-in-exchange.md), [Synchronisieren von Elementänderungen](mailbox-synchronization-and-ews-in-exchange.md) und [Erstellen von benutzerdefinierten Eigenschaftentypen](http://code.msdn.microsoft.com/exchange/Exchange-2013-Create-314db25a)verwenden. Dieser Artikel enthält eine Übersicht über die Eigenschaften und deren Funktionsweise mit Eigenschaften in Ihrer Anwendung.
  
## <a name="exchange-item-properties"></a>Exchange-Elementeigenschaften
<a name="ItemsAreProperties"> </a>

Elemente und Ordner in Exchange bestehen im Wesentlichen aus Zeilen in Tabellen. Die wichtigste Eigenschaft eines Elements oder Ordners ist der [EWS-Bezeichner](ews-identifiers-in-exchange.md). Zwar gibt es andere Bezeichner-bezogene Eigenschaften in der Exchange-Datenbank, der EWS-Bezeichner fungiert für EWS jedoch als Primärschlüssel für die Sammlung von Eigenschaften, die ein Element beschreiben. Die EWS-Bezeichnereigenschaft besteht aus zwei Teilen:
  
- Eine [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)- oder [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)-Eigenschaft, die das Element identifiziert. 
    
- Eine **ChangeKey**-Eigenschaft, die Statusinformationen dazu enthält, ob Änderungen an einem Element oder Ordner vorgenommen wurden. 
    
Alle Elemente in einem Postfach werden in derselben Exchange-Datenbank gespeichert und verwenden dasselbe Datenbankschema. Elemente sind durch eine Kombination aus [ItemClass](http://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx)-Eigenschaft, Eigenschaftsbeschränkungen und Geschäftslogikschichten gekennzeichnet, die deren Verwaltung im Exchange-Speicher beeinflusst. In Tabelle 1 wird dargestellt, wie Eigenschaften über verschiedene Elementtypen hinweg angewendet werden. In diesem Beispiel handelt es sich um E-Mail- und Terminelemente. Beide Elemente verfügen über einen Wert für die [Subject](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx)-Eigenschaft. Beachten Sie jedoch, dass die [IsAllDayEvent](http://msdn.microsoft.com/library/29140a64-9d7a-4a14-a10d-c98197c9831b%28Office.15%29.aspx)-Eigenschaft für das E-Mail-Element und die **IsReadReceiptRequested**-Eigenschaft für das Terminelement nicht festgelegt sind. Glücklicherweise müssen Sie nicht wissen, welche Eigenschaften für welche Elementklasse anwendbar sind; EWS übernimmt dies. 
  
**Tabelle 1. Vergleich von Termin- und E-Mail-Eigenschaften**

|**Elementtyp**|**Elementklasse**|**Betreff**|**IsAllDayEvent**|**IsReadReceiptRequested**|
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

Das EWS-Schema beschreibt die Daten, die zwischen einem EWS-Client und Exchange gesendet werden. Ein großer Teil des Schemas beschreibt die Element- und Ordnereigenschaften, auf die Sie in der Exchange-Datenbank zugreifen können. Das EWS-Schema beschreibt die XML-Darstellung der Exchange-Datenbankeigenschaften, die in Ihrer Anwendung verfügbar sind. Die tatsächlichen Eigenschaften variieren im Hinblick auf die verfügbaren Eigenschaften, die Form und die Rückgabewerte je nachdem, was Sie tun. Die **Body**-Eigenschaft z. B. gibt nur die ersten 512 Zeichen in einem **FindItem**-Vorgang zurück, der **GetItem**-Vorgang gibt jedoch den vollständigen Text des Elements zurück. Obwohl die meisten Eigenschaften festgelegt und abgerufen werden können, werden einige Eigenschaften nur von Exchange festgelegt. Jede Eigenschaft weist im Schema ein XML-Format auf, das die Eigenschaft so widerspiegelt, wie sie in der Exchange-Datenbank gespeichert ist, oder wie sie anhand der in der Exchange-Datenbank gespeicherten Eigenschaften berechnet wurde. Die **Subject**-Eigenschaft stellt ein Beispiel für eine Eigenschaft dar, die festgelegt werden kann; die **UnreadCount**-Eigenschaft eines Ordners stellt ein Beispiel für eine berechnete Eigenschaft dar. Eine Kerngruppe von Eigenschaften haben die Kernelementtypen gemeinsam. 
  
Die folgenden Faktoren bestimmen die festgelegte Eigenschaft, die Ihre Anwendung von Exchange abruft: 
  
- Der Vorgang, den die Anwendung aufruft
    
- Das Basisshape der Antwort
    
- Der Elementtyp
    
- Die angegebenen Eigenschaftspfade
    
Es ist wichtig zu wissen, wie diese verschiedenen Faktoren die Daten beeinflussen, auf die Sie zugreifen können. Wie in dem weiter oben erwähnten Beispiel der **Body**-Eigenschaft, ist die Verfügbarkeit einiger Informationen von verschiedenen Faktoren abhängig. Wenn Sie mit diesen Faktoren vertraut sind, können Sie durch die Auswahl der richtigen Optionen zum Zugreifen auf die gewünschten Informationen Zeit sparen. Zur Ermittlung der Eigenschaften, auf die zugegriffen werden kann, müssen Sie diese Faktoren testen, um festzustellen, wie Sie auf die von Ihrer Anwendung benötigten Eigenschaften zugreifen müssen. In diesem Abschnitt wird beschrieben, wie sich diese verschiedenen Faktoren darauf auswirken, welche Eigenschaften in EWS-Antworten zurückgegeben werden. 
  
### <a name="ews-response-shapes"></a>EWS-Antwortshapes

Exchange speichert eine Vielzahl an Informationen über die Elemente. In manchen Fällen werden nicht alle Informationen für Ihre Anwendung benötigt, manchmal wird sogar empfohlen, nicht alle Informationen abzurufen. [EWS-Antwortshapes](property-sets-and-response-shapes-in-ews-in-exchange.md), auch Eigenschaftsshapes genannt, geben an, welche Eigenschaften vom Server zurückgegeben werden. Das Kernelement des Antwortshapes ist das Basisshape. Beim Basisshape handelt es sich um einen standardmäßig voreingestellten Eigenschaftenbehälter für stark typisierte Elemente. Die Entsprechung des Basisshapes in der EWS Managed API ist [BasePropertySet](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx). EWS umfasst drei standardmäßige Antwortshapes.
  
**Tabelle 2. Standardmäßige Antwortshapes**

|**Name des standardmäßigen Antwortshapes**|**Entsprechung in der verwalteten EWS-API**|**Beschreibung**|
|:-----|:-----|:-----|
|IdOnly  <br/> |BasePropertySet.IdOnly-Wert  <br/> |Es werden nur der EWS-Bezeichner und der Änderungsschlüssel zurückgegeben. Verwenden Sie, wenn der Client nicht alle vom AllProperties- oder Standardshape zurückgegebenen Eigenschaften verwendet, das IdOnly-Shape, und geben Sie weitere Eigenschaften unter Verwendung der Eigenschaftspfade in der **PropertySet**-Klasse an. Die meisten Anwendungen verwenden das IdOnly-Antwortshape mit zusätzlichen Eigenschaften. Dies reduziert den Umfang der nicht verwendeter Daten, die von Clients angefordert werden.  <br/> |
|Standard  <br/> |–  <br/> |Eine Gruppe von Standardeigenschaften für den Elementtyp. Verwenden Sie dieses Antwortshape nur. wenn Ihre Anwendung alle Eigenschaften verwendet.    <br/> |
|AllProperties  <br/> |BasePropertySet.FirstClassProperties-Wert  <br/> |Eine größere Gruppe von Eigenschaften als das Standardshape. Auch wenn der Name dies andeutet, gibt diese Option nicht alle Eigenschaften eines Elements zurück. Dieser Eigenschaftensatz gibt die Eigenschaften zurück, die am häufigsten von Clientanwendungen verwendeten werden. Wenn Sie weitere Eigenschaften benötigen, können Sie diese durch den entsprechenden Eigenschaftspfad anfordern.   <br/> Verwendet Ihre Anwendung nicht alle mit diesem Antwortshape zurückgegebenen Eigenschaften, verwenden Sie das IdOnly-Antwortshape mit zusätzlichen Eigenschaften.  <br/> |
   
Viele EWS-Vorgänge geben Elemente und die zugehörigen Eigenschaften zurück. Unabhängig vom angegebenen Antwortshape, können unterschiedliche Vorgänge unterschiedliche Eigenschaftensätze zurückgeben. Unterschiedliche Elementtypen geben je nach Vorgang und festgelegtem Antwortshape unterschiedliche Eigenschaften zurück. Die folgenden Vorgänge verwenden Antwortshapes, um die zurückzugebenden Eigenschaften zu identifizieren.
  
**Tabelle 3. Vorgänge, die Antwortshapes verwenden**

|**EWS-Vorgang**|**Von EWS verwaltete API-Methode**|
|:-----|:-----|
|[GetConversationItems](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) <br/> |[ExchangeService.GetConversationItems-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) <br/> |
|[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |[Folder.Bind-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> |
|[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |[Item.Bind-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [ExchangeService.BindToItems-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) <br/> |
|[FindConversation](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) <br/> |[ExchangeService.FindConversation-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.findconversation%28v=exchg.80%29.aspx) <br/> |
|[FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |[Folder.FindFolders-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService.FindFolders-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) <br/> |
|[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |[Folder.FindItems-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> [ExchangeService.FindItems-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |
|[FindPeople](http://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) <br/> |Nicht implementiert.  <br/> |
|[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) <br/> |[ExchangeService.ResolveNames-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) <br/> |
|[SearchMailboxes](http://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |[ExchangeService.SearchMailboxes-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.searchmailboxes%28v=exchg.80%29.aspx) <br/> [ExchangeService.BeginSearchMailboxes-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.beginsearchmailboxes%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) <br/> |[ExchangeService.SyncFolderHierarchy-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) <br/> |[ExchangeService.SyncFolderItems-Methode](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) <br/> |
   
Eigenschaftshapes stellen eine elementare Methode dar, um die Eigenschaften zu identifizieren, die Ihre Anwendung zurückgeben soll. In manchen Fällen benötigt Ihre Anwendung jedoch einen begrenzten Satz bestimmter Eigenschaften. Zu diesem Zweck können Sie den Eigenschaftspfad verwenden.
  
### <a name="choose-properties-by-their-property-path"></a>Wählen von Eigenschaften anhand des entsprechenden Eigenschaftspfads

Bei einem EWS-Eigenschaftspfad handelt es sich um Metadaten, die zum Identifizieren von Eigenschaften in einer Anforderung oder Antwort verwendet werden. 
  
**Tabelle 4. Typen von Eigenschaftspfaden**

|**Typ des Eigenschaftspfads**|**Schematyp**|**Implementierung der verwalteten EWS-API**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
|FieldUri  <br/> |PathToUnindexedFieldType  <br/> |Typen, die von [ServiceObjectSchema](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.serviceobjectschema%28v=exchg.80%29.aspx) erben.  <br/> |Der am häufigsten verwendete Eigenschaftspfad. FieldUri-Eigenschaftspfade werden in einem **PropertySet**-Objekt in der verwalteten EWS-API angegeben. Die meisten EWS-Eigenschaften können mit dem FieldUri-Eigenschaftspfad angegeben werden. Dies wird durch das UnindexedFieldURIType-Objekt im EWS-Schema beschrieben.  <br/> Der XML-Code des FieldUri-Eigenschaftspfad sieht wie folgt aus:  <br/> ```XML<FieldURI FieldURI="item:Subject"/>```Dieser Eigenschaftspfad entspricht dem ItemSchema.Subject in der verwalteten EWS-API.  <br/> |
|IndexedFieldUri  <br/> |PathToIndexedFieldType  <br/> |Typen, die von [ItemSchema](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.itemschema%28v=exchg.80%29.aspx) erben.  <br/> |Identifiziert Wörterbucheigenschaften, die einen Eigenschaftenindex erfordern, um den zurückzugebenden Wert anzugeben. Verwenden Sie diesen Pfad, wenn eine Eigenschaft mehr als einen Wert enthalten kann. Dies wird von der **DictionaryURIType**-Eigenschaft im EWS-Schema beschrieben. **DictionaryURIType**-Eigenschaftspfade werden in einem **PropertySet**-Objekt in der verwalteten EWS-API angegeben.  <br/> Der XML-Code des IndexedFieldUri-Eigenschaftspfad sieht wie folgt aus:  <br/> ```XML<IndexedFieldURI FieldURI="contacts:PhysicalAddress:Street FieldIndex="Home"/>```|
|ExtendedFieldUri  <br/> |PathToExtendedFieldType  <br/> |[ExtendedPropertyDefinition](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) <br/> |Gibt eine erweiterte Eigenschaftsdefinition an, die benutzerdefinierte oder nicht schematisierte Eigenschaften von Elementen identifiziert.  <br/> Der XML-Code des ExtendedFieldUri-Eigenschaftspfad sieht wie folgt aus:  <br/> ```XML<ExtendedFieldURI> PropertyTag="0x1234" PropertyType="Integer" />```|
|ExceptionFieldUri  <br/> |ExceptionFieldURI  <br/> |[ServiceResponse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) <br/> |Gibt die Eigenschaften an, die einem Fehler in einer EWS-Antwort zugeordnet sind. Dies wird vom **ExceptionPropertyURIType**-Typ im EWS-Schema beschrieben. Dieser Fehler tritt nur im **MessageXml**-Element der Fehlerantworten auf, die beim Arbeiten mit Kalenderserienmustern auftreten.  <br/> |
   
Verwenden Sie als bewährte Methode beim Anfordern von Eigenschaften das IdOnly-Basisshape ([BasePropertySet.IdOnly](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) in der verwalteten EWS-API), und fordern Sie dann nur die Eigenschaften durch Angeben der Eigenschaftspfade an, die Ihre Anwendung benötigt. 
  
### <a name="schematized-properties"></a>Schematisierte Eigenschaften

Die meisten Eigenschaften, die Ihr EWS-Client benötigt, werden durch das EWS-beschrieben. Die primären Ordner- und Elementtypdefinitionen, die die Eigenschaftsdefinitionen enthalten, sind im Schema „types.xsd“ enthalten. Die folgenden Schematypen enthalten die Eigenschaftsdefinitionen für die meisten Objekte, die Sie verwenden können.
  
**Tabelle 5. Schematypen, die Eigenschaftsdefinitionen enthalten**

|**EWS-Schematyp**|**Typentsprechung in der verwalteten EWS-API**|**Definiert...**|
|:-----|:-----|:-----|
|**ItemType** <br/> |[Elementklasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den Basiselementtyp. Dieser Typ kann von einem Client erstellt werden, wird jedoch nie von Exchange zurückgegeben. Exchange gibt ein MessageType-Objekt für alle generische Objekte zurück.  <br/> |
|**MessageType** <br/> |[EmailMessage-Klasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für das E-Mail-Objekt und alle generischen Objekte.  <br/> |
|**CalendarItemType** <br/> |[Appointment-Klasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den Kalenderelementtyp. Dies umfasst einzelne und wiederkehrende Termine.  <br/> |
|**ContactItemType** <br/> |[Contact-Klasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für das Kontaktelement.  <br/> |
|**DistributionListType** <br/> |[ContactGroup-Klasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für die persönliche Verteilerliste.  <br/> |
|**MeetingMessageType** <br/> |[MeetingMessage-Klasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.meetingmessage%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den Besprechungsnachrichttyp.  <br/> |
|**MeetingRequestMessageType** <br/> |[MeetingRequest-Klasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.meetingrequest%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den Besprechungsanfragentyp.  <br/> |
|**MeetingResponseMessageType** <br/> |[MeetingResponse-Klasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.meetingresponse%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den Besprechungsantworttyp.  <br/> |
|**MeetingCancellationMessageType** <br/> |[MeetingCancellation-Klasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.meetingcancellation%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den Besprechungsabsagentyp.  <br/> |
|**TaskType** <br/> |[Task-Klasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den Aufgabentyp.  <br/> |
|**PostItemType** <br/> |[PostItem-Klasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.postitem%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den Bereitstellungselementtyp.  <br/> |
|**FolderType** <br/> |[Folder-Klasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den Ordnertyp.  <br/> |
|**CalendarFolderType** <br/> |[CalendarFolder-Klasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den SearchFolder-Typ.  <br/> |
|**ContactsFolderType** <br/> |[ContactsFolder-Klasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den ContactsFolder-Typ.  <br/> |
|**SearchFolderType** <br/> |[SearchFolder-Klasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den SearchFolder-Typ.  <br/> |
|**TasksFolderType** <br/> |[TasksFolder-Klasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den TaskFolder-Typ.  <br/> |
|**UserConfigurationType** <br/> |[UserConfiguration-Klasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.userconfiguration%28v=exchg.80%29.aspx) <br/> |den Eigenschaftensatz für den UserConfiguration-Typ.  <br/> |
   
Die Eigenschaften im EWS-Schema sind für viele Anwendungen ausreichend. Manche Szenarien können jedoch nicht ausschließlich unter Verwendung dessen, was im Schema beschrieben ist, implementiert werden. Für diese Szenarien können Sie erweiterte Eigenschaften verwenden. 
  
### <a name="extended-properties-aka-non-schematized-properties"></a>Erweiterte Eigenschaften (auch nicht schematisierte Eigenschaften genannt)

Mit erweiterten Eigenschaften können Sie benutzerdefinierte Eigenschaften erstellen, mit denen Sie auf Elemente und Ordner im Exchange-Speicher zugreifen können, die nicht im EWS-Schema definiert sind. Sie können sie zum Zugreifen auf die Eigenschaften des systemeigenen MAPI-Elements und Ordnereigenschaften in der Exchange-Datenbank verwenden. Mit erweiterten Eigenschaften ist der Zugriff auf alle schematisierten Eigenschaften möglich, da diese schematisierten Eigenschaften nichts Anderes als MAPI-Eigenschaften in der Exchange-Datenbank sind.  
  
Der PathToExtendedFieldType-Schematyp im types.xsd-Schema definiert den XML-Code, der eine erweiterte Eigenschaft darstellt. Dieser Schematyp definiert das [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx)-Element in XML-Instanzen; in anderen Worten, er definiert den XML-Code, der zwischen dem Dienst und dem Client gesendet wird. Der ExtendedPropertyType-Schematyp definiert das [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx)-Element und den Wert oder Array von Werten, den eine erweiterte Eigenschaft enthält. Die folgende Tabelle zeigt die ungefähre Zuordnung des XML-Codes der erweiterten Eigenschaften und die zugehörige Implementierung in Elementen in der EWS Managed API. 
  
**Tabelle 6. Implementierung des XML-Codes der erweiterten Eigenschaften in der verwalteten EWS-API**

|**Implementierung der verwalteten EWS-API**|**Inhalt**|**Zuordnung**|
|:-----|:-----|:-----|
|[Item.ExtendedProperties-Eigenschaft](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.extendedproperties%28v=exchg.80%29.aspx) <br/> |Eine Sammlung erweiterter Eigenschaften eines Elements.  <br/> |Wird einer oder mehreren Instanzen von erweiterten Eigenschaften eines Elements zugeordnet.  <br/> |
|[ExtendedProperty-Eigenschaft](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.extendedproperty%28v=exchg.80%29.aspx) <br/> |Die Definition und Werte der erweiterten Eigenschaft.  <br/> |Wird dem ExtendedPropertyType-Schematyp zugeordnet.  <br/> |
|[ExtendedPropertyDefinition-Eigenschaft](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) <br/> |Die Definition einer erweiterten Eigenschaft.  <br/> |Wird dem PathToExtendedFieldType-Schematyp zugeordnet.  <br/> |
   
Weitere Informationen zum Verwenden erweiterter Eigenschaften in Ihrer Anwendung finden Sie in den folgenden Codebeispielen: 
  
- [MFCMapi](http://mfcmapi.codeplex.com/)
    
- [Exchange 2013: Programmgesteuertes Bereitstellen von benutzerdefinierten X-Headern](http://code.msdn.microsoft.com/exchange/Exchange-2013-Provision-d4ef5719)
    
- [Exchange 2013: Zugreifen auf eine Eigenschaft anhand des zugehörigen Eigenschaftentags](http://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-719875ac)
    
- [Exchange 2013: Zugreifen auf eine benannte Eigenschaft anhand des zugehörigen Bezeichners](http://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-02dbe22f)
    
- [Exchange 2013: Zugreifen auf eine benannte Eigenschaft anhand des zugehörigen Namens](http://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-6556e183)
    
- [Exchange 2013:Zugreifen auf eine Eigenschaft anhand der GUID und des Namens des Eigenschaftensatzes](http://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-4021f971)
    
- [Exchange 2013:Programmgesteuertes Erstellen von benutzerdefinierten erweiterten Eigenschaften](http://code.msdn.microsoft.com/exchange/Exchange-2013-Create-314db25a)
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_inthissection"> </a>

- [Bereitstellen von x-Headern mithilfe von EWS in Exchange](how-to-provision-x-headers-by-using-ews-in-exchange.md)
    
- [Mit der EWS-Eigenschaft zusammenhängende Fehler](ews-property-related-errors.md)
    
## <a name="see-also"></a>Siehe auch


- [Verwenden von Webdiensten in Exchange](start-using-web-services-in-exchange.md)
    
- [MFCMapi](http://mfcmapi.codeplex.com/)
    

