---
title: EWS-Bezeichner in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 39b6b20b-e081-4347-9e15-9b8cf829fdf0
description: Informieren Sie sich über Bezeichner in Exchange und wie Sie diese in Ihren EWS Managed API- und EWS-Anwendungen verwenden können.
ms.openlocfilehash: c09b54c8ec4f443a64f8222094ccf0a5e1f750e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756853"
---
# <a name="ews-identifiers-in-exchange"></a>EWS-Bezeichner in Exchange

Informieren Sie sich über Bezeichner in Exchange und wie Sie diese in Ihren EWS Managed API- und EWS-Anwendungen verwenden können.
  
Jedes Objekt im Exchange-Informationsspeicher verfügt über einen eindeutigen Bezeichner. Sie können den Bezeichner eines Objekts verwenden, um auf das Objekt zu verweisen und es von anderen Objekten zu unterscheiden. Die beiden am häufigsten verwendeten Bezeichner, mit denen Sie möglicherweise arbeiten, sind Ordner- und Elementbezeichner. 
  
Damit Sie verstehen, was Bezeichner sind und warum diese in Ihrer Anwendung wichtig sind, ist es hilfreich, die Beziehung zwischen Objekten in Exchange zu verstehen. Wenn Ihre EWS Managed API- oder EWS-Anwendung mit Exchange kommuniziert, arbeiten Sie mit einer Objekthierarchie, die Postfach-, Ordner- und Elementobjekte enthält. Ein Informationsspeicher kann einen der folgenden Objekttypen aufweisen. In den meisten Fällen ist es ein Postfach auf dem Exchange-Server, aber es kann auch ein öffentlicher Ordner auf dem Exchange-Server sein. (Bedenken Sie, dass bei Exchange Online, Exchange Online als Teil von Office 365 und Exchange-Versionen ab Exchange 2013, öffentliche Ordner lediglich eine andere Art von Postfach und nicht eine andere Art von Informationsspeicher sind.) Der Informationsspeicher enthält Ordner und die Ordner enthalten Elemente, und alle diese Ordner und Elemente weisen einen Bezeichner auf, wie in der folgenden Abbildung dargestellt. 
  
**Abbildung 1. Postfach-, Ordner- und Elementhierarchie**

![Abbildung der Postfachobjekthierarchie. Das Postfach ist auf der obersten Ebene, der Ordner "Posteingang" auf der nächsten Ebene. Das Diagramm zeigt einen Ordner, der E-Mails enthält. IDs und Änderungsschlüssel werden für jedes Objekt gezeigt und sind gekürzt.](media/Ex15_Identifier_diagram.png)
  
## <a name="ews-identifiers"></a>EWS-Bezeichner
<a name="bk_CommonIdentifiers"> </a>

Bezeichner, die EWS für Ordner und Elemente verwendet, werden als EWS-Bezeichner oder EwsIds bezeichnet. EwsIds befinden sich in vielen verschiedenen Objekten innerhalb von EWS, werden jedoch für unterschiedliche Objekte anders bezeichnet. Da Sie diese Objekte möglicherweise in der Anwendung verwenden werden, sollten Sie verstehen, in welcher Beziehung diese Objekte zu der EwsId stehen. 
  
Die Bezeichner in EWS gelten auch für die EWS Managed API. In der EWS Managed API sind die Bezeichner Eigenschaften der Objekte, die intern zur Zuordnung zu den EWS-Elementen verwaltet werden.
  
**Tabelle 1. Objektbezeichner in EWS**

|**Objekt**|**Bezeichner**|**Beziehung zu EwsId**|
|:-----|:-----|:-----|
|[CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) <br/> |Das untergeordnete Element [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) enthält den eindeutigen Bezeichner des Kalenderelements.  <br/> |Das untergeordnete Element [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) ist identisch mit der EwsId für dieses Element.  <br/> |
|[ConversationId](http://msdn.microsoft.com/library/d5f1ddb3-9af3-4677-a6ba-111b304a951e%28Office.15%29.aspx) <br/> |Das **Id**-Attribut enthält den Bezeichner für die Unterhaltung, von der dieses Element ein Teil ist.  <br/> |Das **Id**-Attribut ist identisch mit der EwsId für dieses Element.  <br/> |
|[AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) <br/> |Stellt den eindeutigen Bezeichner der Anlage bereit. Das [RootItemId](http://msdn.microsoft.com/library/f613c705-17ce-48ce-aa64-4dc2cea25e31%28Office.15%29.aspx)-Attribut enthält den eindeutigen Bezeichner des Stamminformationsspeicherelements, an das die Anlage angefügt ist.  <br/> |Anlagen können andere Elemente im Exchange-Informationsspeicher sein. In diesem Fall ist die [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) identisch mit der EwsId. In allen Fällen ist [RootItemId](http://msdn.microsoft.com/library/f613c705-17ce-48ce-aa64-4dc2cea25e31%28Office.15%29.aspx) eine EwsId, da sie auf ein Element im Informationsspeicher verweist.  <br/> |
|[PersonaId](http://msdn.microsoft.com/library/eec3a468-afd5-4d72-a61e-cd1964fb686c%28Office.15%29.aspx) <br/> |Das **Id**-Attribut gibt eine Zeichenfolge zurück, die den Bezeichner der Persona enthält.  <br/> |Das **Id**-Attribut ist identisch mit der EwsId für die Persona.  <br/> |
|[ContactId](http://msdn.microsoft.com/library/86f66275-1e39-48ed-bd89-ac3bffc465a7%28Office.15%29.aspx) <br/> |Das **Id**-Attribut gibt eine Zeichenfolge zurück, die den Bezeichner des Kontakts enthält.  <br/> |Das **Id**-Attribut ist identisch mit der EwsId für den Kontakt.  <br/> |
|[GroupId](http://msdn.microsoft.com/library/656d9b9a-8a65-4a75-8466-5b0d96512dab%28Office.15%29.aspx) <br/> |Das **Id**-Attribut gibt eine Zeichenfolge zurück, die den Bezeichner der Gruppe enthält.  <br/> |Das **Id**-Attribut ist identisch mit der EwsId für die Gruppe.  <br/> |
|[AssociatedCalendarItemId](http://msdn.microsoft.com/library/5b29898c-ea59-4e6a-914c-c011ec754032%28Office.15%29.aspx) <br/> |Die **Id**-Attribut identifiziert das Kalenderelement, das einer [MeetingMessage](http://msdn.microsoft.com/library/c95956a8-7505-44b4-bea4-11d1f5182796%28Office.15%29.aspx), [MeetingRequest](http://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx), [MeetingResponse](http://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx) oder [MeetingCancellation](http://msdn.microsoft.com/library/a9c61f7f-2ecd-4b21-9dce-24d9f61aeeea%28Office.15%29.aspx) zugewiesen ist.  <br/> |Das **Id**-Attribut ist identisch mit der EwsId für das Kalenderelement.  <br/> |
|[UserConfigurationProperties](http://msdn.microsoft.com/library/c143a6ec-62ad-4d48-b844-b1ad88054bc1%28Office.15%29.aspx) <br/> |Der **Id**-Wert für dieses Element gibt die Bezeichnereigenschaft an.  <br/> |Dieser Bezeichner ist nicht direkt der EwsId zugeordnet, da es sich um einen Eigenschaftenbezeichner und nicht um ein Element handelt.  <br/> |
|[OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) <br/> |Das **RecurringMasterId**-Attribut identifiziert den Master eines wiederkehrenden Objekts.  <br/> |Der **OccurrenceItemId**-Wert ist nicht direkt der EwsId zugeordnet, **RecurringMasterId** jedoch schon, da es auf das allgemeine Objekt des wiederkehrenden Objekts verweist.  <br/> |
|[StoreEntryId](http://msdn.microsoft.com/library/f536e264-8c4d-4cc5-bab8-22a4fa38de39%28Office.15%29.aspx) <br/> |Enthält den Bezeichner für den Exchange-Informationsspeicher eines Elements.  <br/> |Der **StoreEntryId**-Wert ist nicht der EwsId zugeordnet, enthält jedoch den Bezeichner des Informationsspeichers, in dem die Elemente gespeichert werden.  <br/> |
   
## <a name="working-with-identifiers"></a>Arbeiten mit Bezeichnern
<a name="bk_WorkingWithIdentifiers"> </a>

Der Exchange-Server verarbeitet Bezeichner auf viele verschiedene Arten. Berücksichtigen Sie beim Entwickeln Ihrer EWS Managed API oder EWS-Anwendung Folgendes:
  
- Bei dem **ItemID** -Elementwert für Ordner und Elemente wird die Groß-/Kleinschreibung beachtet. Wenn Sie sich die Element-ID für einen Ordner oder ein Element ansehen, der bzw. das von der [FindItem-Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) (oder der [FindItems ](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)-Methode der EWS Managed API) zurückgegeben wird, denken Sie vielleicht, dass es sich um ein Duplikat einer anderen Element-ID handelt; ein oder mehrere Zeichen in den Element-IDs für die beiden Elemente weisen jedoch eine andere Schreibweise auf. 
    
- Wenn die Element-ID in einer Datenbank zum späteren Abrufen speichern, empfehlen wir, die Feldgröße auf 512 Bytes festzulegen, damit es groß genug für die GUID ist.
    
- Gehen Sie nicht davon aus, dass Ihre ID immer gültig ist, wenn Sie das Element zu einem späteren Zeitpunkt abrufen müssen. Wenn ein Element im Speicher verschoben wird, kann sich die ID aufgrund der Verschiebung ändern. Ein Element wird tatsächlich kopiert, und es wird eine neue ID generiert, und dann [wird das ursprüngliche Element gelöscht](deleting-items-by-using-ews-in-exchange.md).
    
- Bezeichner in Exchange sind nicht transparent. Die EwsId wird z. B. aus mehreren Datenelementen erstellt, die für Sie als Entwickler nicht wichtig sind, für Exchange jedoch schon.
    
- Wenn Sie mit Elementen in Exchange arbeiten, müssen Sie auch das **ChangeKey**-Attribut beachten. Dieser Wert wird neben der Element-ID verwendet, um den Status eines Elements nachzuverfolgen. Jedes Mal, wenn ein Element geändert wird, wird ein neuer Änderungsschlüssel generiert. Beim Ausführen einer [UpdateItem Operation](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) können Sie das **ChangeKey**-Attribut zum Beispiel verwenden, um dem Server mitzuteilen, dass die Aktualisierung auf die aktuellste Version des Elements angewendet wird. Wenn eine andere Anwendung eine Änderung an dem Element vorgenommen hat, das Sie aktualisieren, stimmen die Änderungsschlüssel nicht überein, und Sie können die Aktualisierung nicht durchzuführen. 
    
## <a name="distinguished-folder-ids"></a>IDs des definierten Ordners
<a name="bk_DistinguishedFolderIds"> </a>

Exchange umfasst eine Vielzahl vordefinierter Postfachordnen angezeigt, von denen jedem ein Bezeichner zugeordnet wird, der als die ID des definierten Ordner bezeichnet wird. Diese werden von der [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)-Enumeration der EWS Managed API und dem [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx)-Element von EWS definiert. Sie können diese IDs des definierten Ordners verwenden, um einfacher auf einen der vordefinierten Ordner zu verweisen. Für den Ordner "Posteingang" können Sie zum Beispiel einfach "Posteingang" für den Bezeichner verwenden, anstatt den Ordnerbezeichner zu ermitteln. 
  
Andere Ordner, die Sie zum Organisieren von E-Mail-Elementen erstellen, weisen auch eine ID auf, die für diesen Ordner eindeutig ist. Diese ID ändert sich nicht, selbst wenn Sie andere Eigenschaften des Ordners ändern.
  
Sie können IDs des definierten Ordners als Einstiegspunkt für Zugriffsrechte für Stellvertretung verwenden. Wenn Sie Zugriffsrechte für Stellvertretung initiieren, suchen Sie nach Elementen oder Ordnern, und geben die ID des definierten Ordners an, um den Suchbereich anzugeben. Wenn ein Stellvertreter auf den Server zugreift, wird ein [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)-Element, das ein untergeordnetes Element des **DistinguishedFolderId**-Elements ist, verwendet, um das Postfach, auf das der Stellvertreter zugreifen kann, explizit anzugeben. 
  
## <a name="handling-errors"></a>Behandeln von Fehlern
<a name="bk_DealingWithErrors"> </a>

In jedem Programm wird hin und wieder ein Fehler angezeigt, und EWS-basierte Anwendungen sind keine Ausnahme (Wortspiel beabsichtigt). Möglicherweise werden einige Fehler in Bezug auf IDs im EWS-Element [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) oder im Rahmen der [ServiceError](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx)-Aufzählung der EWS Managed API angezeigt. 
  
Die folgenden Fehler können in der EWS Managed API- oder EWS-Anwendung auftreten: Wenn Sie mit einer EWS Managed API-Anwendung arbeiten, handelt es sich bei den Fehlern in der Regel um Probleme mit Eigenschaftenwerten. Bei EWS-Anwendungen stehen die Fehler im Zusammenhang mit XML-Elementwerten oder -Operationen.
  
**Tabelle 2. Fehler im Zusammenhang mit Bezeichnern**

|**Fehler**|**Tritt auf**|**Beschreibung**|
|:-----|:-----|:-----|
|ErrorCalendarCannotUseIdForOccurrenceId  <br/> |Der Wert von **OccurenceID** entspricht nicht einer gültigen Terminserie des Kalenders.  <br/> |Der Wert von **OccurenceId**, der in der Anforderung angegeben wurde, ist möglicherweise in der Struktur gültig, die Anforderung konnte jedoch keine Übereinstimmung mit einem wiederkehrenden Master finden. Die Terminserie wurde möglicherweise aus dem Kalender entfernt. Stellen Sie sicher, dass das Element immer noch vorhanden ist und dass Sie den korrekten Bezeichner verwenden.  <br/> |
|ErrorCalendarCannotUseIdForRecurringMasterId  <br/> |Das **RecurringMasterId**-Attribut entspricht keinem gültigen Vorkommnis des **OccurrenceId**-Elements.  <br/> |Der Wert von **RecurringMasterId**, der in der Anforderung angegeben wurde, ist möglicherweise in der Struktur gültig, die Anforderung konnte jedoch keine Übereinstimmung mit einem vorhandenen Vorkommnis des Elements finden. Die Vorkommnis des Elements wurde möglicherweise aus dem Kalender entfernt. Stellen Sie sicher, dass das Element immer noch vorhanden ist und dass Sie den korrekten Bezeichner verwenden.  <br/> |
|ErrorCannotUseFolderIdForItemId  <br/> |Das übergebene **ID** stellt einen Ordner anstelle eines Elements dar.  <br/> |Das Format des Bezeichners ist möglicherweise gültig, entspricht aber nicht den Erwartungen des Servers für den Vorgang. Stellen Sie sicher, dass Sie auf den korrekten Bezeichner für den Vorgang verweisen.  <br/> |
|ErrorCannotUseItemIdForFolderId  <br/> |Das übergebene **ID** stellt einen Ordner anstelle eines Elements dar.  <br/> |Das Format des Bezeichners ist möglicherweise gültig, entspricht aber nicht den Erwartungen des Servers für den Vorgang. Stellen Sie sicher, dass Sie auf den korrekten **ID** für den Vorgang verweisen.  <br/> |
|ErrorChangeKeyRequiredForWriteOperations  <br/> |Beim Ausführen bestimmter Aktualisierungsvorgänge muss ein gültiger Schlüssel angegeben werden.  <br/> |Sie haben beim Anfordern einer Aktualisierung entweder einen **ChangeKey**-Wert vergessen oder der Änderungsschlüssel war falsch. Stellen Sie sicher, dass Sie über den richtigen Änderungsschlüssel verfügen, wenn Sie Aktualisierungsvorgänge ausführen.  <br/> |
|ErrorInvalidAttachmentId  <br/> |Die Anlage wurde nicht in der Anlagensammlung für das Element gefunden.  <br/> |Dieser Antwortcode wird möglicherweise angezeigt, wenn Sie eine Anlage **ID** haben und die Anlage wird gelöscht wird, und Sie versuchen, rufen Sie die [GetAttachment-Vorgang](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) für die Anlagen-ID aufzurufen. Stellen Sie sicher, dass die Anlage in der Anlagensammlung vorhanden ist.  <br/> |
|ErrorInvalidChangeKey  <br/> |Ein ungültiger Änderungsschlüssel wurde übergeben.  <br/> |Beachten Sie, dass es für viele Vorgänge und Methoden nicht erforderlich ist, einen Änderungsschlüssel zu übergeben. Wenn Sie jedoch einen Änderungsschlüssel angeben, muss er gültig, aber nicht unbedingt aktuell sein.  <br/> |
|ErrorInvalidFolderId  <br/> |Der Ordner **ID** ist beschädigt.  <br/> |Stellen Sie sicher, dass Sie über einen korrekt formatierten und gültigen Bezeichner verfügen.  <br/> |
|ErrorInvalidId  <br/> |Die Struktur des **ID** und/oder des Änderungsschlüssels ist intern inkonsistent.  <br/> |Exchange hat ein Problem mit **ID** nach der Analyse festgestellt. Möglicherweise ist ein Fehler bei der Konvertierung aufgetreten. Dies kann z. B. auftreten, wenn Sie einen **IdFormatType.HexEntryId** für ein Element in Outlook haben, diesen aber in eine EwsId konvertieren, weil Sie davon ausgegangen sind, dass es sich um ein **IdFormatType.EntryId**-Format handelte. Stellen Sie sicher, dass Sie den richtigen Konvertierungstyp verwenden.  <br/> |
|ErrorInvalidIdEmpty  <br/> |Die Anwendung hat einen **ID**, der leer ist.  <br/> |Die Anwendung hat eine leere Zeichenfolge für den Bezeichner angegeben. Stellen Sie sicher, dass Sie über einen korrekt formatierten und gültigen Bezeichner verfügen.  <br/> |
|ErrorInvalidIdMalformed  <br/> |Die Struktur von **ID** ist intern inkonsistent.  <br/> |Exchange hat ein Problem mit **ID** nach der Analyse festgestellt. Die ID wurde möglicherweise nicht ordnungsgemäß konvertiert. Stellen Sie sicher, dass Sie den richtigen Konvertierungstyp verwenden.  <br/> |
|ErrorInvalidIdMalformedEwsLegacyIdFormat  <br/> |Ein Ordner oder ein Element **ID**, der bzw. das das Exchange 2007-Format verwendet, wurde für eine Anforderung mit einer Version von Exchange 2007 SP1 oder höher angegeben.    <br/> |Sie können Exchange 2007-IDs nicht in Anforderungen mit Exchange 2007 SP1 oder höher verwenden. Sie müssen die EWS-Operation[ConvertId](http://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx) oder die EWS Managed API-Methode [ConvertId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.convertid%28v=exchg.80%29.aspx) verwenden, um diese zuerst zu konvertieren.  <br/> |
|ErrorInvalidIdNotAnItemAttachmentId  <br/> |Die **AttachmentId**-Eigenschaft verweist nicht auf eine Elementanlage.  <br/> |Das Format des Bezeichners ist möglicherweise gültig, entspricht aber nicht den Erwartungen des Servers für den Vorgang. Stellen Sie sicher, dass Sie auf den korrekten Bezeichner für den Vorgang verweisen.  <br/> |
|ErrorInvalidIdReturnedByResolveNames  <br/> |Ein Kontakt in Ihrem Postfach ist beschädigt.  <br/> |Die EWS-Operation [ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx)oder die EWS Managed API-Methode [ResolveName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) hat eine oder mehrere Bezeichner zurückgegeben, diese sind aber nicht gültig. Möglicherweise müssen Sie den Kontakt neu erstellen.  <br/> |
|ErrorInvalidIdStoreObjectIdTooLong  <br/> |Die Struktur von **ID** ist intern inkonsistent.  <br/> |Exchange hat ein Problem mit **ID** nach der Analyse festgestellt. Die **ID** wurde möglicherweise nicht ordnungsgemäß konvertiert. Stellen Sie sicher, dass Sie den richtigen Konvertierungstyp verwenden.  <br/> |
|ErrorInvalidIdTooManyAttachmentLevels  <br/> |Die Anlagenhierarchien überschreiten die maximale Tiefe von 255 Ebenen.  <br/> |Der Wert der **AttachmentId**-Eigenschaft, der in der Anforderung angegeben wurde, ist in der Struktur möglicherweise gültig, in der Hierarchie ist die angeforderte Anlage jedoch zu tief. Der Code hat möglicherweise versucht, ein Element jenseits der Grenze von 255 Ebenen anzufügen.  <br/> |
|ErrorInvalidImContactId  <br/> |Dieser Fehler kann zurückgegeben werden, wenn der Kontakt bei Verwendung der [RemoveImContactFromGroup-Vorgang](http://msdn.microsoft.com/library/a190bbec-c71b-4e6a-880b-55854c724d8c%28Office.15%29.aspx) in der Sofortnachrichtengruppe nicht gefunden werden kann. Dieser Fehler tritt bei Clients auf, die auf Exchange Online und Exchange-Versionen ab Exchange 2013 abzielen.  <br/> |Der Wert der **ContactId**-Eigenschaft, der in der Anforderung angegeben wurde, ist in der Struktur möglicherweise gültig, im Postfach stimmen jedoch keine Kontakte mit dieser Struktur überein. Der Kontakt wurde möglicherweise bereits entfernt.  <br/> |
|ErrorInvalidImGroupId  <br/> |Dieser Fehler kann zurückgegeben werden, wenn der Kontakt bei Verwendung der [RemoveImGroup-Vorgang](http://msdn.microsoft.com/library/5e788016-68e0-4a3f-9243-03f6b6c6b389%28Office.15%29.aspx) nicht im Postfach gefunden werden kann. Dieser Fehler tritt bei Clients auf, die auf Exchange Online und Exchange-Versionen ab Exchange 2013 abzielen.  <br/> |Der Wert der **GroupId**-Eigenschaft, der in der Anforderung angegeben wurde, ist in der Struktur möglicherweise gültig, im Postfach stimmen jedoch keine Gruppen mit dieser Struktur überein. Die Gruppe wurde möglicherweise bereits entfernt.  <br/> |
|ErrorInvalidReferenceItem  <br/> |Der Elementbezeichner, auf den verwiesen wird, ist kein **MessageType** oder **ExchangeWebServices.CalendarItemTypeType** oder ein untergeordnetes Elemente davon. Das Elementbezeichner, auf den verwiesen wird, ist für ein **CalendarItemType**-Objekt, und der Organisator versucht zu antworten bzw. allen zu antworten.  <br/> |Das Format des Bezeichners ist möglicherweise gültig, entspricht aber nicht den Erwartungen des Servers für den Vorgang. Stellen Sie sicher, dass Sie auf den korrekten Bezeichner für den Vorgang verweisen.  <br/> |
|ErrorMissingManagedFolderId  <br/> |Die Eigenschaft von Richtlinie IDs, Eigenschaftentag 0x6732, für den Ordner ist nicht vorhanden.  <br/> |Der Ordner ist beschädigt. Sie sollten ihn neu erstellen.  <br/> |
   
## <a name="converting-identifiers"></a>Konvertieren von Bezeichnern
<a name="bk_ConvertingIdentifiers"> </a>

Möglicherweise müssen Sie einen Bezeichner von einem Format in ein anderes konvertieren. Beispielsweise müssen Sie vielleicht einen Bezeichner von außerhalb von EWS, z. B. ein Bezeichner, der aus einer MAPI-Verbindung stammt, in ein Format konvertieren, das Ihre Anwendung verwenden kann. Hierfür können Sie die EWS-Operation [ConvertId](http://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx) oder die EWS Managed API-Methode [ConvertId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.convertid%28v=exchg.80%29.aspx) verwenden. 
  
Eine EntryID ist z. B. ein eindeutiger Bezeichner, der vom MAPI-Nachrichtenspeicher generiert wird, der vom Speicher zugewiesen wird, wenn das Element gespeichert wird. Um eine EntryID in der Anwendung zu verwenden, müssen Sie sie zuerst in eine EwsId konvertieren. 
  
Outlook Web App verwendet eine eigene Version von Bezeichnern, genannt OwaId, in URLs, um auf Ordner und Elemente zuzugreifen. Wenn Ihre Anwendung auf in Outlook Web App zugreifen muss, müssen Sie die OwaId in eine EwsId konvertieren.
  
Sie können die **ConvertId**-Operation oder -Methode verwenden, um mehrere unterschiedliche Bezeichnerformate zu konvertieren. 
  
**Tabelle 3. Konvertierbare Bezeichnerformate in Exchange**

|**Format**|**Beschreibung**|
|:-----|:-----|
|EwsLegacyId  <br/> |Die EwsId, die für Exchange 2007 gilt.  <br/> |
|EwsId  <br/> |Die EwsId, die für Exchange Online und Exchange-Versionen ab Exchange 2007 SP1 gilt.  <br/> |
|StoreId  <br/> |Der Bezeichner für den Exchange-Informationsspeicher, in dem die Ordner und Elemente gespeichert werden.  <br/> |
|OwaId  <br/> |Der Outlook Web App-Bezeichner, der bei Outlook Web App in Exchange 2007 und Exchange Server 2010 verwendet wird.  <br/> > [!NOTE]> Exchange Online und Exchange beginnend mit Exchange 2013-Versionen verwenden die EwsId für Outlook Web App.           |
|EntryId  <br/> |Ein MAPI-Bezeichner, der allgemein als die **PR_ENTRYID** -Eigenschaft einer MAPI-Nachricht bekannt ist.  <br/> |
|HexEntryId  <br/> |Eine hexadezimal codierte Darstellung der **PR_ENTRYID** -Eigenschaft, die für den Ereignisbezeichner des Verfügbarkeitskalenders verwendet wird. Dies ist auch das Bezeichnerformat, das Outlook verwendet.  <br/> |
   
## <a name="see-also"></a>Siehe auch


- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [ConvertId-Vorgang](http://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx)
    
- [ServiceError-Aufzählung](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx)
    
- [Löschen von Elementen mithilfe von EWS in Exchange](deleting-items-by-using-ews-in-exchange.md)
    

