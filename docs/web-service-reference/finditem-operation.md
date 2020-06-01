---
title: FindItem-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- FindItem
api_type:
- schema
ms.assetid: ebad6aae-16e7-44de-ae63-a95b24539729
description: Informationen zum FindItem-EWS-Vorgang.
localization_priority: Priority
ms.openlocfilehash: 499d1ee80ef323c883fa86eb125d8c037fb37d4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462556"
---
# <a name="finditem-operation"></a>FindItem-Vorgang

Informationen zum **FindItem**-EWS-Vorgang. 
  
Der **FindItem**-Vorgang durchsucht Elemente im Benutzerpostfach. Dieser Vorgang bietet viele Möglichkeiten zum Filtern und Formatieren der im Aufrufer zurückgegebenen Suchergebnisse. 
  
## <a name="using-the-finditem-operation"></a>Verwenden des FindItem-Vorgangs

Der **FindItem**-Vorgangsanforderung bietet zahlreiche Möglichkeiten zum Durchsuchen eines Postfachs und zum Formatieren der in einer Antwort zurückgegebenen Suchergebnisse. Sie können folgende Parameter in einer **FindItem**-Anforderung festlegen: 
  
- Ob die Suche mit flachen Einschränkungen durchgeführt und ob die Ergebnisse vorläufig gelöscht werden sollen. Erforderlich. Beachten Sie, dass eine Suche mit vorläufig zu löschenden Ergebnissen und einer Sucheinschränkung keine Elemente zurückgibt, wenn Elemente vorhanden sind, die den Suchkriterien entsprechen.
    
- Das Antwortshape von Elementen. Identifiziert die Eigenschaften, die in der Antwort zurückgegeben werden. Erforderlich.
    
- Die Ordner, für die die Suche durchgeführt werden soll. Erforderlich.
    
- Seitennummerierungsmechanismus und Ansichtstypen für das Zurückgeben von Daten auf Seiten. Optional.
    
- Optionen zum Gruppieren und Sortieren der Elemente, die zurückgegeben werden. Optional.
    
- Sucheinschränkungen oder AQS-Zeichenfolgen zum Filtern der Elemente, die zurückgegeben werden. Weitere Informationen zur Verwendung von AQS für Inhaltsindexsuchen finden Sie unter [QueryString (Zeichenfolge)](querystring-string.md). Optional.
    
- Die Sortierreihenfolge für die in einer Antwort zurückgegebenen Elemente. Optional.
    
Der **FindItem**-Vorgang gibt nur die ersten 512 Byte einer beliebigen streamfähigen Eigenschaft zurück. Bei Unicode werden nur die ersten 255 Zeichen mit einer Unicode-Zeichenfolge zurückgegeben, die mit null endet. Es werden keine Nachrichtentextformate oder Empfängerlisten zurückgegeben. **FindItem** gibt eine Empfängerübersicht zurück. Sie können den [GetItem Operation](getitem-operation.md) zum Abrufen von Details eines Elements verwenden. 
  
 **FindItem** gibt nur das [Name (EmailAddressType)](name-emailaddresstype.md)-Element zurück und gibt kein [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)-Element im [Postfach](mailbox.md)-Element für die folgenden Felder zurück: 
  
- Das Feld [Von](from.md) für Nachrichten 
    
- Das Feld [Absender](sender.md) für Nachrichten 
    
- Das Feld [Organisator](organizer.md) für die Elemente im Kalender 
    
> [!NOTE]
> Der **FindItem**-Vorgang kann Ergebnisse in einem [CalendarView](calendarview.md)-Element zurückgeben. Das **CalendarView**-Element gibt einzelne Kalenderelemente und alle Vorkommen wiederkehrender Besprechungen zurück. Wenn ein **CalendarView**-Element nicht verwendet wird, werden einzelne Kalenderelemente und wiederkehrende Masterterminserien zurückgegeben. Die Vorkommen müssen von der Masterterminserie aus erweitert werden, wenn ein **CalendarView**-Element nicht verwendet wird. 
  
Der **FindItem**-Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
**Tabelle 1. SOAP-Header im FindItem-Vorgang**

|**Header**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**DateTimePrecision** <br/> |[DateTimePrecision](datetimeprecision.md) <br/> |Gibt die Auflösung der Daten-/Uhrzeitwerte in Antworten vom Server an, entweder in Sekunden oder in Millisekunden. Dies gilt für eine Anforderung.  <br/> |
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dies gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Gibt die RFC3066-Kultur an, die für den Zugriff auf das Postfach verwendet wird. Dies gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Dies gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dies gilt für eine Antwort.  <br/> |
|**TimeZoneContext** <br/> |[TimeZoneContext](timezonecontext.md) <br/> |Gibt die Zeitzone für alle Antworten vom Server an. Dies gilt für eine Anforderung.  <br/> |
   
## <a name="finditem-operation-request-example"></a>Beispiel für eine FindItem-Vorgangsanforderung

Im folgenden Beispiel einer **FindItem**-Anforderung wird das Abrufen des Elementbezeichners erläutert, der in der **IdOnly** -Enumeration des [BaseShape](baseshape.md)-Elements für Elemente im Ordner „Gelöschte Elemente" definiert ist. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
              Traversal="Shallow">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </ItemShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="deleteditems"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

In der Anforderung werden folgende Elemente verwendet: 
  
- [FindItem](finditem.md)
    
- [ItemShape](itemshape.md)
    
- [BaseShape](baseshape.md)
    
- [ParentFolderIds](parentfolderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
Weitere Optionen für eine **FindItem**-Anforderungsnachricht finden Sie in der Schemahierarchie. Beginnen Sie beim [FindItem](finditem.md)-Element. 
  
## <a name="successful-finditem-operation-response"></a>Antwort bei einem erfolgreichen FindItem-Vorgang

Im folgenden Beispiel wird eine erfolgreiche Antwort auf eine **FindItem**-Anforderung veranschaulicht. 
  
[Message](message-ex15websvcsotherref.md) -Elemente stellen E-Mails und alle anderen Elemente dar, die durch das EWS-Schema nicht stark typisiert werden. Elemente wie IPM.Sharing- und IPM.InfoPath-Elemente werden als [Message](message-ex15websvcsotherref.md)-Elemente zurückgegeben. Exchange gibt das [Element](item.md)-Basiselement nicht in Antworten zurück. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="10" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AS4AUn=" ChangeKey="fsVU4==" />
              </t:Message>
              <t:Message>
                <t:ItemId Id="AS4AUM=" ChangeKey="fsVUA==" />
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </FindItemResponse>
  </soap:Body>
</soap:Envelope>
```

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [FindItemResponse](finditemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [FindItemResponseMessage](finditemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md)
    
- [Elemente](items.md)
    
- [Message](message-ex15websvcsotherref.md)
    
- [ItemId](itemid.md)
    
Weitere Optionen für eine **FindItem**-Antwortnachricht finden Sie in der Schemahierarchie. Beginnen Sie beim [FindItemResponse](finditemresponse.md)-Element. 
  
## <a name="finditem-operation-error-response"></a>Fehlerantwort bei einem FindItem-Vorgang

Im folgenden Beispiel wird eine Fehlerantwort bei einer **FindItem**-Anforderung veranschaulicht. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </FindItemResponse>
  </soap:Body>
</soap:Envelope>
```

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [FindItemResponse](finditemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [FindItemResponseMessage](finditemresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Weitere Optionen für eine **FindItem**-Fehlerantwortnachricht finden Sie in der Schemahierarchie. Beginnen Sie beim [FindItemResponse](finditemresponse.md)-Element. 
  
## <a name="version-differences"></a>Versionsunterschiede

Exchange-Versionen ab Hauptversion 15, die mit Build 15.0.898.11 enden, geben einen ErrorInvalidOperation-Wert im [ResponseCode](responsecode.md)-Element zurück, wenn der **FindItem**-Vorgang zum Durchsuchen mehrerer Ordner in einem Archivpostfach verwendet wird. 
  
## <a name="see-also"></a>Siehe auch

- [Suchen von Elementen](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)
    
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
    
- **FindItemType**
    

