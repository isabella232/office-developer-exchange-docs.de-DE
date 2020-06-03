---
title: GetServerTimeZonesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServerTimeZonesResponse
api_type:
- schema
ms.assetid: 97c94d32-10f1-4c3e-ab20-9fd7e8257e50
description: Das GetServerTimeZonesResponse-Element definiert eine Antwort auf eine GetServerTimeZones-Vorgangsanforderung.
ms.openlocfilehash: 5a8dbe19055e3b697149c10df610d081cb65430b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460925"
---
# <a name="getservertimezonesresponse"></a><span data-ttu-id="19e74-103">GetServerTimeZonesResponse</span><span class="sxs-lookup"><span data-stu-id="19e74-103">GetServerTimeZonesResponse</span></span>

<span data-ttu-id="19e74-104">Das **GetServerTimeZonesResponse** -Element definiert eine Antwort auf eine [GetServerTimeZones-Vorgangs](getservertimezones-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="19e74-104">The **GetServerTimeZonesResponse** element defines a response to a [GetServerTimeZones operation](getservertimezones-operation.md) request.</span></span> 
  
```XML
<GetServerTimeZonesResponse>
   <ResponseMessages/>
</GetServerTimeZonesResponse>
```

 <span data-ttu-id="19e74-105">**GetServerTimeZonesResponseType**</span><span class="sxs-lookup"><span data-stu-id="19e74-105">**GetServerTimeZonesResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="19e74-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="19e74-106">Attributes and elements</span></span>

<span data-ttu-id="19e74-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="19e74-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19e74-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="19e74-108">Attributes</span></span>

<span data-ttu-id="19e74-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="19e74-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="19e74-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="19e74-110">Child elements</span></span>

|<span data-ttu-id="19e74-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="19e74-111">**Element**</span></span>|<span data-ttu-id="19e74-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="19e74-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19e74-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="19e74-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="19e74-114">Enthält die Antwortnachrichten für eine Exchange Webdienste-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="19e74-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="19e74-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="19e74-115">Parent elements</span></span>

<span data-ttu-id="19e74-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="19e74-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="19e74-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19e74-117">Remarks</span></span>

<span data-ttu-id="19e74-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="19e74-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="19e74-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="19e74-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19e74-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="19e74-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="19e74-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="19e74-121">Schema Name</span></span>  <br/> |<span data-ttu-id="19e74-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="19e74-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="19e74-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="19e74-123">Validation File</span></span>  <br/> |<span data-ttu-id="19e74-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="19e74-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="19e74-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="19e74-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="19e74-126">False</span><span class="sxs-lookup"><span data-stu-id="19e74-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="19e74-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19e74-127">See also</span></span>



- [<span data-ttu-id="19e74-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="19e74-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

