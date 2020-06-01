---
title: ConvertIdResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertIdResponse
api_type:
- schema
ms.assetid: ac1f044f-04a4-42ef-b762-cac5cd37894d
description: Das ConvertIdResponse-Element enthält eine Antwort auf eine Convert-Anforderung. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 690f0f2109dfc36dd8f359b7cef1e65beb47fc6e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452524"
---
# <a name="convertidresponse"></a><span data-ttu-id="c6c7e-104">ConvertIdResponse</span><span class="sxs-lookup"><span data-stu-id="c6c7e-104">ConvertIdResponse</span></span>

<span data-ttu-id="c6c7e-105">Das **ConvertIdResponse** -Element enthält eine Antwort auf eine Convert-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-105">The **ConvertIdResponse** element contains a response to a ConvertId request.</span></span> <span data-ttu-id="c6c7e-106">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ConvertIdResponse>
   <ResponseMessages/>
</ConvertIdResponse>
```

 <span data-ttu-id="c6c7e-107">**ConvertIdResponseType**</span><span class="sxs-lookup"><span data-stu-id="c6c7e-107">**ConvertIdResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c6c7e-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c6c7e-108">Attributes and elements</span></span>

<span data-ttu-id="c6c7e-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6c7e-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="c6c7e-110">Attributes</span></span>

<span data-ttu-id="c6c7e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c6c7e-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c6c7e-112">Child elements</span></span>

|<span data-ttu-id="c6c7e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c6c7e-113">**Element**</span></span>|<span data-ttu-id="c6c7e-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c6c7e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6c7e-115">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c6c7e-115">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="c6c7e-116">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-116">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c6c7e-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c6c7e-117">Parent elements</span></span>

<span data-ttu-id="c6c7e-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c6c7e-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6c7e-119">Remarks</span></span>

<span data-ttu-id="c6c7e-120">Die Antwortnachrichten, die im [ResponseMessages](responsemessages.md) -Element enthalten sind, werden Instanzen von ConvertIdResponseMessageType sein.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-120">The response messages that are contained within the [ResponseMessages](responsemessages.md) element will be instances of ConvertIdResponseMessageType.</span></span> 
  
<span data-ttu-id="c6c7e-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c6c7e-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c6c7e-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6c7e-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="c6c7e-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c6c7e-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c6c7e-124">Schema Name</span></span>  <br/> |<span data-ttu-id="c6c7e-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c6c7e-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c6c7e-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c6c7e-126">Validation File</span></span>  <br/> |<span data-ttu-id="c6c7e-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c6c7e-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c6c7e-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c6c7e-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="c6c7e-129">False</span><span class="sxs-lookup"><span data-stu-id="c6c7e-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c6c7e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6c7e-130">See also</span></span>



[<span data-ttu-id="c6c7e-131">ConvertId-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c6c7e-131">ConvertId operation</span></span>](convertid-operation.md)


- [<span data-ttu-id="c6c7e-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c6c7e-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="c6c7e-133">Konvertieren von Bezeichnern</span><span class="sxs-lookup"><span data-stu-id="c6c7e-133">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

