---
title: UnsubscribeResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnsubscribeResponse
api_type:
- schema
ms.assetid: 125e0326-6522-42cd-b20e-6977e6fde249
description: Das UnsubscribeResponse-Element definiert eine Antwort auf eine unsubscribe-Anforderung.
ms.openlocfilehash: 1a8ddf93499acb7aa369ec9e91a7106e5cb4bd53
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467200"
---
# <a name="unsubscriberesponse"></a><span data-ttu-id="8b43e-103">UnsubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="8b43e-103">UnsubscribeResponse</span></span>

<span data-ttu-id="8b43e-104">Das **UnsubscribeResponse** -Element definiert eine Antwort auf eine unsubscribe-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8b43e-104">The **UnsubscribeResponse** element defines a response to an Unsubscribe request.</span></span> 
  
```xml
<UnsubscribeResponse>
   <ResponseMessages/>
</UnsubscribeResponse>
```

 <span data-ttu-id="8b43e-105">**UnsubscribeResponseType**</span><span class="sxs-lookup"><span data-stu-id="8b43e-105">**UnsubscribeResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8b43e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8b43e-106">Attributes and elements</span></span>

<span data-ttu-id="8b43e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8b43e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8b43e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8b43e-108">Attributes</span></span>

<span data-ttu-id="8b43e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8b43e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8b43e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8b43e-110">Child elements</span></span>

|<span data-ttu-id="8b43e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8b43e-111">**Element**</span></span>|<span data-ttu-id="8b43e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8b43e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8b43e-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8b43e-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="8b43e-114">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8b43e-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8b43e-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8b43e-115">Parent elements</span></span>

<span data-ttu-id="8b43e-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="8b43e-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8b43e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b43e-117">Remarks</span></span>

<span data-ttu-id="8b43e-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="8b43e-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8b43e-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="8b43e-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8b43e-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b43e-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8b43e-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8b43e-121">Schema name</span></span>  <br/> |<span data-ttu-id="8b43e-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8b43e-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8b43e-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8b43e-123">Validation file</span></span>  <br/> |<span data-ttu-id="8b43e-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="8b43e-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8b43e-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8b43e-125">Can be empty</span></span>  <br/> |<span data-ttu-id="8b43e-126">False</span><span class="sxs-lookup"><span data-stu-id="8b43e-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8b43e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b43e-127">See also</span></span>



- [<span data-ttu-id="8b43e-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8b43e-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

