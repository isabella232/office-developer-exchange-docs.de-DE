---
title: DeleteItemResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItemResponse
api_type:
- schema
ms.assetid: 86463d66-fe47-4a19-a81b-e24841e816ab
description: Das DeleteItemResponse-Element definiert eine Antwort auf eine einzelne DeleteItem an.
ms.openlocfilehash: 8a35033c744fbcb0829d2c79a8d79557f77137bb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757929"
---
# <a name="deleteitemresponse"></a><span data-ttu-id="53a05-103">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="53a05-103">DeleteItemResponse</span></span>

<span data-ttu-id="53a05-104">Das **DeleteItemResponse** -Element definiert eine Antwort auf eine einzelne DeleteItem an.</span><span class="sxs-lookup"><span data-stu-id="53a05-104">The **DeleteItemResponse** element defines a response to a single DeleteItem request.</span></span> 
  
```xml
<DeleteItemResponse>
   <ResponseMessages/>
</DeleteItemResponse>
```

 <span data-ttu-id="53a05-105">**DeleteItemResponseType**</span><span class="sxs-lookup"><span data-stu-id="53a05-105">**DeleteItemResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="53a05-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="53a05-106">Attributes and elements</span></span>

<span data-ttu-id="53a05-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="53a05-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53a05-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="53a05-108">Attributes</span></span>

<span data-ttu-id="53a05-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="53a05-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="53a05-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="53a05-110">Child elements</span></span>

|<span data-ttu-id="53a05-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="53a05-111">**Element**</span></span>|<span data-ttu-id="53a05-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="53a05-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53a05-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="53a05-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="53a05-114">Enthält die Antwortnachrichten für eine Exchange-Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="53a05-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="53a05-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="53a05-115">Parent elements</span></span>

<span data-ttu-id="53a05-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="53a05-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="53a05-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="53a05-117">Remarks</span></span>

<span data-ttu-id="53a05-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="53a05-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="53a05-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="53a05-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53a05-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="53a05-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="53a05-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="53a05-121">Schema Name</span></span>  <br/> |<span data-ttu-id="53a05-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="53a05-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="53a05-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="53a05-123">Validation File</span></span>  <br/> |<span data-ttu-id="53a05-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="53a05-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="53a05-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="53a05-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="53a05-126">False</span><span class="sxs-lookup"><span data-stu-id="53a05-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53a05-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53a05-127">See also</span></span>

- [<span data-ttu-id="53a05-128">DeleteItem-Operation</span><span class="sxs-lookup"><span data-stu-id="53a05-128">DeleteItem operation</span></span>](deleteitem-operation.md)  
- [<span data-ttu-id="53a05-129">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="53a05-129">DeleteItem</span></span>](deleteitem.md)
- [<span data-ttu-id="53a05-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="53a05-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

