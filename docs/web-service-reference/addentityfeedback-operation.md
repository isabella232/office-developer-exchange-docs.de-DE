---
title: AddEntityFeedback-Vorgang
manager: luken
ms.date: 4/18/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 00e40197-5794-4268-b937-bd65aa044890
description: Der Vorgang AddEntityFeedback gibt entsprechend der serverseitigen Probleme Fehlerinformationen zurück.
ms.openlocfilehash: b695806f543827d78aea139ffcbd7e4af58b9fef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757227"
---
# <a name="addentityfeedback-operation"></a>AddEntityFeedback-Vorgang

Der Vorgang **AddEntityFeedback** gibt entsprechend der serverseitigen Probleme Fehlerinformationen zurück. 
  
Dieser Vorgang basiert auf den Typ des Ereignisses protokolliert wird. Eines der wichtigsten Ereignisse ist **EntityAdded**, der auf eine Entität auswahlwahrscheinlichkeit entspricht. Dieser Vorgang ist Batch, damit dieser Batches von Einträgen in einer einzelnen Anforderung erfassen verwendet werden kann. 
  
## <a name="findpeople-request-examples"></a>FindPeople-anforderungsbeispiele

Der Vorgang **AddEntityFeedback** bietet eine Möglichkeit für Clients, um die Details der Interaktion mit Entitäten, die vom Dienst zurückgegebenen melden. Dies kann als Signal zur Verbesserung der Relevanz im Hintergrund für jeden Client verwendet werden. Z. B. können Clients diesen Vorgang Sie Feedback geben möchten auf Personen Entitäten, die von **FindPeople**zurückgegeben.
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
                             xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                             xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="the-request-soap-body-contents"></a>Die Anforderung SOAP-Body-Inhalt

Die Soap-Anforderung enthält ein einzelnes Element **EntityFeedbackEntries**. Dies enthält wiederum ein Array von **EntityFeedbackEntry** -Objekten. Jeder Eintrag im Array kann die folgenden Elemente enthalten. 
  
|**Anforderungsparameter**|**Erforderlich**|**Beschreibung**|**Typ**|
|:-----|:-----|:-----|:-----|
|**ClientEventTimeUtc** <br/> |Ja  <br/> |Die UTC-Zeit, die das Ereignis auf der Clientseite aufgetreten ist.  <br/> |DateTime  <br/> |
|**ClientEventTimeLocal** <br/> |Ja  <br/> |Die lokale Uhrzeit des Ereignisses auf dem Client aufgetreten ist.  <br/> |DateTime  <br/> |
|**ClientId** <br/> |Ja  <br/> |Der Typ des Clients (z. B. Outlook, OWA usw.).  <br/> |ClientIDType-Aufzählung  <br/> |
|**ClientSessionId** <br/> |Ja  <br/> |GUID, identifiziert die ID der Sitzung. Auf dem Client generiert.  <br/> |GUID  <br/> |
|**ClientVersion** <br/> |Ja  <br/> |Version des Clients (z. B. 15.01.0101.000).  <br/> |Zeichenfolge  <br/> |
|**EntityAddSource** <br/> |Nein  <br/> |Quelle für EntityAded (z. B., EntityRelevanceAPI, Typen, eingefügt werden).  <br/> |EntityAddSource-Aufzählung  <br/> |
|**EntrySequenceNumber** <br/> |Ja  <br/> |Inkrementelle eine ganze Zahl pro Sitzung. Zum Auffinden von Datenverlusten verwendet.  <br/> |Int  <br/> |
|**EventType** <br/> |Ja  <br/> |Typ des Ereignisses (z. B., Entität hinzugefügt, entfernt Entität).  <br/> |Zeichenfolge  <br/> |
|**JSONPropertyBag** <br/> |Nein  <br/> |Zusätzliche Eigenschaften, die das Ereignis (JSON Blob Schlüssel/Wert-Paare) zugeordnet.  <br/> |JSON Blob  <br/> |
|**TargetEntityList** <br/> |Nein  <br/> |Liste der Entitäten, die mit dem Ereignis verknüpft ist.  <br/> |JSON-Zeichenfolge  <br/> |
|**Transaktions-ID** <br/> |Nein  <br/> |ID (GUID) korrelieren der ID im abfrageprotokolle.  <br/> |Zeichenfolge  <br/> |
   
### <a name="successful-addentityfeedback-operation-response"></a>Erfolgreiche AddEntityFeedback Vorgangsantwort

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                                MinorVersion="1" 
                                MajorBuildNumber="228" 
                                MinorBuildNumber="0" 
                                Version="V2_49" 
                                xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                                xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" 
                                                              xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                                              xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                                              xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope> 

```

### <a name="the-response-soap-body-contains-the-following-elements"></a>Die Antwort SOAP-Text enthält die folgenden Elemente

#### <a name="errors"></a>Fehler 
  
Die API ein Batches von Feedback Einträge melden kann, wir melden alle, die wir können. Dieses Feld stellt die Anzahl der Fehlereinträge, die nicht protokolliert wurden.
    
#### <a name="errordetails"></a>ErrorDetails
  
Einzelheiten zu den oben genannten Fehler durch trennt `;`.
    
### <a name="currently-supported-values"></a>Derzeit unterstützte Werte

|**ClientIdType-Aufzählung**|
|:-----|
|Desktop  <br/> |
|Exchange  <br/> |
|IMAP4  <br/> |
|Lync  <br/> |
|MacMail  <br/> |
|MacOutlook  <br/> |
|Mobil  <br/> |
|Andere  <br/> |
|Outlook  <br/> |
|OutlookService  <br/> |
|POP3  <br/> |
|Tablet  <br/> |
|Web  <br/> |
   
|**EntityAddSource-Aufzählung**|
|:-----|
|ActiveDirectory-Umgebung  <br/> |
|EntityRelevanceApi  <br/> |
|EntityRelevanceApiCache  <br/> |
|ExplicitTyping  <br/> |
|LocalCache  <br/> |
|LocalCacheAndEntityRelevanceAPI  <br/> |
|Keine  <br/> |
|Andere  <br/> |
|Einfügen  <br/> |
   
### <a name="addentityfeedback-operation-error-response"></a>AddEntityFeedback Vorgang Fehlerantwort

Fehlercodes, die für EWS generisch sind, finden Sie unter [ResponseCode](responsecode.md).
  
### <a name="example-of-addentityfeedback-in-conjunction-with-findpeople"></a>Beispiel für AddEntityFeedback in Verbindung mit FindPeople

#### <a name="findpeople-request"></a>FindPeople Anforderung
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

#### <a name="findpeople-response"></a>FindPeople Antwort

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <FindPeopleResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <People>
                <Persona xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

#### <a name="addentityfeedback-request"></a>AddEntityFeedback Anforderung

```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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
> Antwort Transaktions-ID als die AddEntityFeedback Anforderungstransaktion mit FindPeople-ID. 
  
#### <a name="addentityfeedback-response"></a>AddEntityFeedback Antwort

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope>

```


