---
title: SendItemResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendItemResponse
api_type:
- schema
ms.assetid: 26ac41c7-57d9-473e-ab7a-bae93e1d2aba
description: Das SendItemResponse-Element definiert eine Antwort auf eine SendItem-Anforderung.
ms.openlocfilehash: dd90510547c3db8c3531663c23d05055bd774fab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462129"
---
# <a name="senditemresponse"></a><span data-ttu-id="d666b-103">SendItemResponse</span><span class="sxs-lookup"><span data-stu-id="d666b-103">SendItemResponse</span></span>

<span data-ttu-id="d666b-104">Das **SendItemResponse** -Element definiert eine Antwort auf eine SendItem-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d666b-104">The **SendItemResponse** element defines a response to a SendItem request.</span></span> 
  
```xml
<SendItemResponse>
   <ResponseMessages/>
</SendItemResponse>
```

 <span data-ttu-id="d666b-105">**SendItemResponseType**</span><span class="sxs-lookup"><span data-stu-id="d666b-105">**SendItemResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d666b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d666b-106">Attributes and elements</span></span>

<span data-ttu-id="d666b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d666b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d666b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d666b-108">Attributes</span></span>

<span data-ttu-id="d666b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d666b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d666b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d666b-110">Child elements</span></span>

|<span data-ttu-id="d666b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d666b-111">**Element**</span></span>|<span data-ttu-id="d666b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d666b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d666b-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d666b-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="d666b-114">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d666b-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d666b-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d666b-115">Parent elements</span></span>

<span data-ttu-id="d666b-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="d666b-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d666b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d666b-117">Remarks</span></span>

<span data-ttu-id="d666b-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d666b-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d666b-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d666b-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d666b-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="d666b-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d666b-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d666b-121">Schema name</span></span>  <br/> |<span data-ttu-id="d666b-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d666b-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d666b-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d666b-123">Validation file</span></span>  <br/> |<span data-ttu-id="d666b-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d666b-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d666b-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d666b-125">Can be empty</span></span>  <br/> |<span data-ttu-id="d666b-126">False</span><span class="sxs-lookup"><span data-stu-id="d666b-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d666b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d666b-127">See also</span></span>



[<span data-ttu-id="d666b-128">SendItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d666b-128">SendItem operation</span></span>](senditem-operation.md)
  
[<span data-ttu-id="d666b-129">SendItem</span><span class="sxs-lookup"><span data-stu-id="d666b-129">SendItem</span></span>](senditem.md)


- [<span data-ttu-id="d666b-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d666b-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

