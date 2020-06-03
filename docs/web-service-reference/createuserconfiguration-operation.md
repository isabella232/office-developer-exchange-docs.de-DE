---
title: CreateUserConfiguration-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateUserConfiguration
api_type:
- schema
ms.assetid: eb5b8ab6-9743-481c-aac9-f9aa889bd353
description: Mit dem CreateUserConfiguration-Vorgang wird ein Benutzer Konfigurationsobjekt für einen Ordner erstellt.
ms.openlocfilehash: 0c9233146d21c7014be15896426b968106485200
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463783"
---
# <a name="createuserconfiguration-operation"></a><span data-ttu-id="6a645-103">CreateUserConfiguration-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6a645-103">CreateUserConfiguration operation</span></span>

<span data-ttu-id="6a645-104">Mit dem **CreateUserConfiguration** -Vorgang wird ein Benutzer Konfigurationsobjekt für einen Ordner erstellt.</span><span class="sxs-lookup"><span data-stu-id="6a645-104">The **CreateUserConfiguration** operation creates a user configuration object on a folder.</span></span> 
  
## <a name="createuserconfiguration-request-example"></a><span data-ttu-id="6a645-105">CreateUserConfiguration-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="6a645-105">CreateUserConfiguration request example</span></span>

### <a name="description"></a><span data-ttu-id="6a645-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a645-106">Description</span></span>

<span data-ttu-id="6a645-107">Im folgenden Beispiel einer **CreateUserConfiguration** -Anforderung wird gezeigt, wie Sie eine Anforderung zum Erstellen eines Benutzer Konfigurationsobjekts im Ordner "Entwürfe" bilden.</span><span class="sxs-lookup"><span data-stu-id="6a645-107">The following example of a **CreateUserConfiguration** request shows how to form a request to create a user configuration object on the Drafts folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="6a645-108">Code</span><span class="sxs-lookup"><span data-stu-id="6a645-108">Code</span></span>

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
    <m:CreateUserConfiguration>
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
    </m:CreateUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

## <a name="createuserconfiguration-response-example"></a><span data-ttu-id="6a645-109">CreateUserConfiguration-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="6a645-109">CreateUserConfiguration response example</span></span>

### <a name="description"></a><span data-ttu-id="6a645-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a645-110">Description</span></span>

<span data-ttu-id="6a645-111">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die **CreateUserConfiguration** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6a645-111">The following example shows a successful response to the **CreateUserConfiguration** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="6a645-112">Code</span><span class="sxs-lookup"><span data-stu-id="6a645-112">Code</span></span>

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
    <m:CreateUserConfigurationResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateUserConfigurationResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:CreateUserConfigurationResponseMessage>
      </m:ResponseMessages>
    </m:CreateUserConfigurationResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="6a645-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a645-113">See also</span></span>



[<span data-ttu-id="6a645-114">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="6a645-114">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="6a645-115">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6a645-115">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

