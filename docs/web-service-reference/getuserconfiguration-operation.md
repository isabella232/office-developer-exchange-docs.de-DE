---
title: GetUserConfiguration-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserConfiguration
api_type:
- schema
ms.assetid: 71d50e3c-92bd-435f-8118-b28bb85f8138
description: Der GetUserConfiguration-Vorgang ruft ein Benutzer Konfigurationsobjekt aus einem Ordner ab.
ms.openlocfilehash: fb28e88d1a47b0ea8f63ed33b1efacae8538e1c8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458208"
---
# <a name="getuserconfiguration-operation"></a><span data-ttu-id="e0f57-103">GetUserConfiguration-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e0f57-103">GetUserConfiguration operation</span></span>

<span data-ttu-id="e0f57-104">Der **GetUserConfiguration** -Vorgang ruft ein Benutzer Konfigurationsobjekt aus einem Ordner ab.</span><span class="sxs-lookup"><span data-stu-id="e0f57-104">The **GetUserConfiguration** operation gets a user configuration object from a folder.</span></span> 
  
## <a name="getuserconfiguration-request-example"></a><span data-ttu-id="e0f57-105">GetUserConfiguration-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="e0f57-105">GetUserConfiguration request example</span></span>

### <a name="description"></a><span data-ttu-id="e0f57-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0f57-106">Description</span></span>

<span data-ttu-id="e0f57-107">Im folgenden Beispiel einer **GetUserConfiguration** -Anforderung wird gezeigt, wie eine Anforderung zum Abrufen eines Benutzer Konfigurationsobjekts im Ordner "Entwürfe" erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e0f57-107">The following example of a **GetUserConfiguration** request shows how to form a request to get a user configuration object on the Drafts folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e0f57-108">Code</span><span class="sxs-lookup"><span data-stu-id="e0f57-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:GetUserConfiguration>
      <m:UserConfigurationName Name="TestConfig">
        <t:DistinguishedFolderId Id="drafts"/>
      </m:UserConfigurationName>
      <m:UserConfigurationProperties>Dictionary</m:UserConfigurationProperties>
    </m:GetUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

## <a name="getuserconfiguration-response-example"></a><span data-ttu-id="e0f57-109">GetUserConfiguration-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="e0f57-109">GetUserConfiguration response example</span></span>

### <a name="description"></a><span data-ttu-id="e0f57-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0f57-110">Description</span></span>

<span data-ttu-id="e0f57-111">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die **GetUserConfiguration** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e0f57-111">The following example shows a successful response to the **GetUserConfiguration** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="e0f57-112">Code</span><span class="sxs-lookup"><span data-stu-id="e0f57-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetUserConfigurationResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetUserConfigurationResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:UserConfiguration>
            <t:UserConfigurationName Name="TestConfig">
              <t:DistinguishedFolderId Id="drafts">
              </t:DistinguishedFolderId>
            </t:UserConfigurationName>
            <t:Dictionary>
              <t:DictionaryEntry>
                <t:DictionaryKey>
                  <t:Type>String</t:Type>
                  <t:Value>PhoneNumber</t:Value>
                </t:DictionaryKey>
                <t:DictionaryValue>
                  <t:Type>String</t:Type>
                  <t:Value>555-555-1111</t:Value>
                </t:DictionaryValue>
              </t:DictionaryEntry>
            </t:Dictionary>
          </m:UserConfiguration>
        </m:GetUserConfigurationResponseMessage>
      </m:ResponseMessages>
    </m:GetUserConfigurationResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="e0f57-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0f57-113">See also</span></span>



[<span data-ttu-id="e0f57-114">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="e0f57-114">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="e0f57-115">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e0f57-115">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

