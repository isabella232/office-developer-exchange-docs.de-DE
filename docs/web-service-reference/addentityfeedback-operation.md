---
title: AddEntityFeedback-Vorgang
manager: luken
ms.date: 4/18/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 00e40197-5794-4268-b937-bd65aa044890
description: Der AddEntityFeedback-Vorgang gibt Fehlerinformationen zurück, die serverseitigen Problemen entsprechen.
ms.openlocfilehash: d4322bcc075c8c68b1f3d5f2ae22badea02be452
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546826"
---
# <a name="addentityfeedback-operation"></a>AddEntityFeedback-Vorgang

Der **AddEntityFeedback-Vorgang** gibt Fehlerinformationen zurück, die serverseitigen Problemen entsprechen. 
  
Dieser Vorgang basiert auf dem Typ des protokollierten Ereignisses. Eines der wichtigsten Ereignisse ist **EntityAdded**, das einer ausgewählten Entität entspricht. Dieser Vorgang ist ein Batch, sodass er zum Protokollieren von Batches von Einträgen in einer einzigen Anforderung verwendet werden kann. 
  
## <a name="findpeople-request-examples"></a>FindPeople-Anforderungsbeispiele

Der **AddEntityFeedback-Vorgang** bietet Clients eine Möglichkeit, Details der Interaktion mit entitäten zu protokollieren, die vom Dienst zurückgegeben werden. Dies kann als Signal verwendet werden, um die Relevanz im Hintergrund für jeden Client zu verbessern. Beispielsweise können Clients diesen Vorgang verwenden, um Feedback zu Personenentitäten zu geben, die von **FindPeople** zurückgegeben wurden.
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
                             xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                             xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:AddEntityFeedback>
            <m:EntityFeedbackEntries>
                  <t:EntityFeedbackEntry>
                        <t:ClientEventTimeUTC> 2015-07-05T22:16:18+00:00</t:ClientEventTimeUTC>
                        <t:ClientEventTimeLocal> 2015-07-05T22:16:18+00:00</t:ClientEventTimeLocal>
                        <t:ClientSessionId>00000000-0000-0000-0000-000000000012</t:ClientSessionId>
                        <t:ClientVersion>15.01.0101.01</t:ClientVersion>
                        <t:ClientId>Web</t:ClientId>
                        <t:TransactionId>123456789</t:TransactionId>
                        <t:EventType>EntityAdded</t:EventType>
                        <t:TargetEntityList>["a","b","c"]</t:TargetEntityList>
                        <t:SourceOfEntityAdded></t:SourceOfEntityAdded>
                        <t:JSONPropertyBag></t:JSONPropertyBag>
                  </t:EntityFeedbackEntry>
                  <t:EntityFeedbackEntry>
                  …
                  </t:EntityFeedbackEntry>
            </m:EntityFeedbackEntries>
      </m:AddEntityFeedback>
   </soap:Body>
</soap:Envelope>

```

### <a name="the-request-soap-body-contents"></a>Inhalt des SOAP-Textkörpers der Anforderung

Die Soap-Anforderung enthält ein einzelnes Element **EntityFeedbackEntries**. Diese wiederum enthält ein Array von **EntityFeedbackEntry-Objekten.** Jeder Eintrag im Array kann die folgenden Elemente enthalten. 
  
|**Anforderungsparameter**|**Erforderlich**|**Beschreibung**|**Typ**|
|:-----|:-----|:-----|:-----|
|**ClientEventTimeUtc** <br/> |Ja  <br/> |Die UTC-Zeit, zu der das Ereignis auf clientseitiger Seite aufgetreten ist.  <br/> |DateTime  <br/> |
|**ClientEventTimeLocal** <br/> |Ja  <br/> |Die Ortszeit, zu der das Ereignis auf clientseitiger Seite aufgetreten ist.  <br/> |DateTime  <br/> |
|**Clientid** <br/> |Ja  <br/> |Typ des Clients (z. B. Outlook, OWA usw.).  <br/> |ClientIDType-Enumeration  <br/> |
|**ClientSessionId** <br/> |Ja  <br/> |GUID, die die Sitzungs-ID identifiziert. Generiert auf dem Client.  <br/> |GUID  <br/> |
|**ClientVersion** <br/> |Ja  <br/> |Version des Clients (z. B. 15.01.0101.000).  <br/> |String  <br/> |
|**EntityAddSource** <br/> |Nein  <br/> |Quelle für EntityAded (z. B. EntityRelevanceAPI, Typen, eingefügt).  <br/> |EntityAddSource-Enumeration  <br/> |
|**EntrySequenceNumber** <br/> |Ja  <br/> |Eine inkrementelle ganze Zahl pro Clientsitzung. Wird zum Erkennen von Datenverlust verwendet.  <br/> |Int  <br/> |
|**EventType** <br/> |Ja  <br/> |Ereignistyp (z. B. Entität hinzugefügt, Entität entfernt).  <br/> |String  <br/> |
|**JSONPropertyBag** <br/> |Nein  <br/> |Zusätzliche Eigenschaften, die dem Ereignis zugeordnet sind (JSON-Blob von Schlüssel-Wert-Paaren).  <br/> |JSON Blob  <br/> |
|**TargetEntityList** <br/> |Nein  <br/> |Liste der Entitäten, die dem Ereignis zugeordnet sind.  <br/> |JSON-Zeichenfolge  <br/> |
|**TransactionId** <br/> |Nein  <br/> |ID (GUID), die die ID in Abfrageprotokollen korreliert.  <br/> |String  <br/> |
   
### <a name="successful-addentityfeedback-operation-response"></a>Erfolgreiche AddEntityFeedback-Vorgangsantwort

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                                MinorVersion="1" 
                                MajorBuildNumber="228" 
                                MinorBuildNumber="0" 
                                Version="V2_49" 
                                xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                                xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" 
                                                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                                              xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                                              xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope> 

```

### <a name="the-response-soap-body-contains-the-following-elements"></a>Der SOAP-Antworttext enthält die folgenden Elemente

#### <a name="errors"></a>Fehler 
  
Die API kann einen Batch von Feedbackeinträgen protokollieren, wir protokollieren alles, was möglich ist. Dieses Feld stellt die Anzahl der Fehlereinträge dar, die nicht protokolliert wurden.
    
#### <a name="errordetails"></a>ErrorDetails
  
Details zu den obigen Fehlern werden durch `;` getrennt.
    
### <a name="currently-supported-values"></a>Derzeit unterstützte Werte

|**ClientIdType-Enumeration**|
|:-----|
|Desktop  <br/> |
|Exchange  <br/> |
|IMAP4  <br/> |
|Lync  <br/> |
|MacMail  <br/> |
|MacOutlook  <br/> |
|Mobilgeräte  <br/> |
|Sonstiges  <br/> |
|Outlook  <br/> |
|OutlookService  <br/> |
|POP3  <br/> |
|Tablet  <br/> |
|Netz  <br/> |
   
|**EntityAddSource-Enumeration**|
|:-----|
|Activedirectory  <br/> |
|EntityRelevanceApi  <br/> |
|EntityRelevanceApiCache  <br/> |
|ExplicitTyping  <br/> |
|LocalCache  <br/> |
|LocalCacheAndEntityRelevanceAPI  <br/> |
|Keines  <br/> |
|Sonstiges  <br/> |
|Einfügen  <br/> |
   
### <a name="addentityfeedback-operation-error-response"></a>Fehlerantwort des AddEntityFeedback-Vorgangs

Fehlercodes, die für EWS generisch sind, finden Sie unter [ResponseCode](responsecode.md).
  
### <a name="example-of-addentityfeedback-in-conjunction-with-findpeople"></a>Beispiel für AddEntityFeedback in Verbindung mit FindPeople

#### <a name="findpeople-request"></a>FindPeople-Anforderung
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
<soap:Body >
    <m:FindPeople>
      <m:IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="100" Offset="0"/>
      <m:QueryString>user1</m:QueryString>
      <m:SearchPeopleSuggestionIndex>true</m:SearchPeopleSuggestionIndex>
    </m:FindPeople>
  </soap:Body>
</soap:Envelope>    
    
```

#### <a name="findpeople-response"></a>FindPeople-Antwort

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <FindPeopleResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <People>
                <Persona xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                    <PersonaId Id="AAUQAFjZ4UxX8SZCqSPFsmh0cSo=" />
                    <PersonaType>Person</PersonaType>
                    <CreationTime>2015-10-02T23:25:42</CreationTime>
                    <DisplayName>user2</DisplayName>
…
                  </Persona>
            </People>
            <TotalNumberOfPeopleInView>0</TotalNumberOfPeopleInView>
            <FirstMatchingRowIndex>0</FirstMatchingRowIndex>
            <FirstLoadedRowIndex>0</FirstLoadedRowIndex>
            <TransactionId>b56ad16e-5d5a-4574-90f8-b8dd57382be6</TransactionId>
        </FindPeopleResponse>
    </s:Body>
</s:Envelope>

```

#### <a name="addentityfeedback-request"></a>AddEntityFeedback-Anforderung

```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:AddEntityFeedback>
<m:EntityFeedbackEntries>
<t:EntityFeedbackEntry>
         <t:ClientEventTimeUtc>2015-07-05T22:16:18+00:00</t:ClientEventTimeUtc>
         <t:ClientEventTimeLocal>2015-07-05T22:16:18+00:00</t:ClientEventTimeLocal>
         <t:ClientSessionId>00000000-0000-0000-0000-000000000012</t:ClientSessionId>
         <t:ClientVersion>15.01.0101.01</t:ClientVersion>
         <t:ClientId>Web</t:ClientId>
         <t:TransactionId>b56ad16e-5d5a-4574-90f8-b8dd57382be6</t:TransactionId>
         <t:EventType>EntityAdded</t:EventType>
         <t:TargetEntityList>["user1@ms7.com"]</t:TargetEntityList>
         <t:SourceOfEntityAdded>EntityRelevanceApi</t:SourceOfEntityAdded>
         <t:JSONPropertyBag></t:JSONPropertyBag>
</t:EntityFeedbackEntry>
</m:EntityFeedbackEntries>
      </m:AddEntityFeedback>
   </soap:Body>
</soap:Envelope>

```

> [!NOTE]
> Verwenden der FindPeople-Antworttransaktions-ID als Transaktions-ID der AddEntityFeedback-Anforderung. 
  
#### <a name="addentityfeedback-response"></a>AddEntityFeedback-Antwort

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope>

```


