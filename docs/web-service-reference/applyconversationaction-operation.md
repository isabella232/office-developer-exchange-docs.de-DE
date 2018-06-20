---
title: ApplyConversationAction-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ApplyConversationAction
api_type:
- schema
ms.assetid: 73d7943d-d361-4f8b-9948-d85f886efa1a
description: Der Vorgang ApplyConversationAction legt einen einmaligen oder Nachfassen Aktion bei allen Elementen in einer Unterhaltung. Der Vorgang ApplyConversationAction können Sie kategorisieren, verschieben, kopieren, löschen und Festlegen der Zustand "gelesen" für alle Elemente in einer Unterhaltung. Aktionen können auch in einer Unterhaltung neue Nachrichten festgelegt werden.
ms.openlocfilehash: 2a485b84ee87aec2ed807e3f4f0901b83432fa0a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757308"
---
# <a name="applyconversationaction-operation"></a><span data-ttu-id="8bc45-105">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8bc45-105">ApplyConversationAction operation</span></span>

<span data-ttu-id="8bc45-106">Der Vorgang **ApplyConversationAction** legt einen einmaligen oder Nachfassen Aktion bei allen Elementen in einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="8bc45-106">The **ApplyConversationAction** operation sets a one-time or follow up action on all the items in a conversation.</span></span> <span data-ttu-id="8bc45-107">Der Vorgang **ApplyConversationAction** können Sie kategorisieren, verschieben, kopieren, löschen und Festlegen der Zustand "gelesen" für alle Elemente in einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="8bc45-107">The **ApplyConversationAction** operation allows you to categorize, move, copy, delete, and set the read state on all items in a conversation.</span></span> <span data-ttu-id="8bc45-108">Aktionen können auch in einer Unterhaltung neue Nachrichten festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8bc45-108">Actions can also be set for new messages in a conversation.</span></span> 
  
## <a name="applyconversationaction-request-example"></a><span data-ttu-id="8bc45-109">Anforderungsbeispiel ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="8bc45-109">ApplyConversationAction request example</span></span>

### <a name="description"></a><span data-ttu-id="8bc45-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8bc45-110">Description</span></span>

<span data-ttu-id="8bc45-111">Im folgenden Beispiel wird einer Anforderung **ApplyConversationAction** veranschaulicht, wie Elemente in der angegebenen Unterhaltung in einen anderen Ordner verschoben.</span><span class="sxs-lookup"><span data-stu-id="8bc45-111">The following example of an **ApplyConversationAction** request shows how to move the items in the specified conversation to another folder.</span></span> <span data-ttu-id="8bc45-112">Elemente, die die Unterhaltung hinzugefügt werden, werden auch in den angegebenen Ordner verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="8bc45-112">Items that are added to the conversation will also be moved to the specified folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="8bc45-113">Code</span><span class="sxs-lookup"><span data-stu-id="8bc45-113">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:ApplyConversationAction>
      <m:ConversationActions>
        <t:ConversationAction>
          <t:Action>AlwaysMove</t:Action>
          <t:ConversationId Id="AAQkADVkNjM1EH39AWcDUGrnrnJ32hHpdc="/>
          <t:DestinationFolderId>
            <t:FolderId Id="AAMkADVkNjM1ODI3LTEwYTAtNDUBTTT6tWal35iSoKAAAABZZWAAA="/>
          </t:DestinationFolderId>
        </t:ConversationAction>
      </m:ConversationActions>
    </m:ApplyConversationAction>
  </soap:Body>
</soap:Envelope>
```

### <a name="remarks"></a><span data-ttu-id="8bc45-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8bc45-114">Remarks</span></span>

<span data-ttu-id="8bc45-115">Der Bezeichner Unterhaltung und Ordner wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8bc45-115">The conversation and folder identifiers have been shortened to preserve readability.</span></span>
  
## <a name="applyconversationaction-response-example"></a><span data-ttu-id="8bc45-116">ApplyConversationAction antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="8bc45-116">ApplyConversationAction response example</span></span>

### <a name="description"></a><span data-ttu-id="8bc45-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8bc45-117">Description</span></span>

<span data-ttu-id="8bc45-118">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **ApplyConversationAction** .</span><span class="sxs-lookup"><span data-stu-id="8bc45-118">The following example shows a successful response to an **ApplyConversationAction** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="8bc45-119">Code</span><span class="sxs-lookup"><span data-stu-id="8bc45-119">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="1" 
                         MajorBuildNumber="91" 
                         MinorBuildNumber="0" 
                         Version="Exchange2010_SP1" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:ApplyConversationActionResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:ApplyConversationActionResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:ApplyConversationActionResponseMessage>
      </m:ResponseMessages>
    </m:ApplyConversationActionResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="8bc45-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bc45-120">See also</span></span>

- [<span data-ttu-id="8bc45-121">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8bc45-121">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="8bc45-122">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="8bc45-122">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
- [<span data-ttu-id="8bc45-123">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8bc45-123">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="8bc45-124">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="8bc45-124">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

