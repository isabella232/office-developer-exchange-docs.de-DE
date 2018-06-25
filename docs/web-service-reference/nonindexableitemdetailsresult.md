---
title: NonIndexableItemDetailsResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7cbdbc21-5405-4cbc-8ca0-d7b0257927aa
description: Das NonIndexableItemDetailsResult-Element gibt die Ergebnisse des GetNonIndexableItemDetails WSDL-Vorgangs.
ms.openlocfilehash: 6e271f2cf0e37f26b945332c94167b6a42354115
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830535"
---
# <a name="nonindexableitemdetailsresult"></a><span data-ttu-id="268fc-103">NonIndexableItemDetailsResult</span><span class="sxs-lookup"><span data-stu-id="268fc-103">NonIndexableItemDetailsResult</span></span>

<span data-ttu-id="268fc-104">Das **NonIndexableItemDetailsResult** -Element gibt die Ergebnisse des **GetNonIndexableItemDetails** WSDL-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="268fc-104">The **NonIndexableItemDetailsResult** element specifies the results of the **GetNonIndexableItemDetails** WSDL operation.</span></span> 
  
```XML
<NonIndexableItemDetailsResult>
   <Items/>
   <FailedMailboxes/>
</NonIndexableItemDetailsResult>
```

 <span data-ttu-id="268fc-105">**NonIndexableItemDetailResultType**</span><span class="sxs-lookup"><span data-stu-id="268fc-105">**NonIndexableItemDetailResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="268fc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="268fc-106">Attributes and elements</span></span>

<span data-ttu-id="268fc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="268fc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="268fc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="268fc-108">Attributes</span></span>

<span data-ttu-id="268fc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="268fc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="268fc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="268fc-110">Child elements</span></span>

<span data-ttu-id="268fc-111">[Elemente (ArrayOfNonIndexableItemDetailsType)](items-arrayofnonindexableitemdetailstype.md) , [FailedMailboxes](failedmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="268fc-111">[Items (ArrayOfNonIndexableItemDetailsType)](items-arrayofnonindexableitemdetailstype.md) , [FailedMailboxes](failedmailboxes.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="268fc-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="268fc-112">Parent elements</span></span>

<span data-ttu-id="268fc-113">[GetNonIndexableItemDetailsResponse](getnonindexableitemdetailsresponse.md) , [GetNonIndexableItemDetailsResponseMessage](getnonindexableitemdetailsresponsemessage.md)</span><span class="sxs-lookup"><span data-stu-id="268fc-113">[GetNonIndexableItemDetailsResponse](getnonindexableitemdetailsresponse.md) , [GetNonIndexableItemDetailsResponseMessage](getnonindexableitemdetailsresponsemessage.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="268fc-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="268fc-114">Remarks</span></span>

<span data-ttu-id="268fc-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="268fc-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="268fc-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="268fc-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="268fc-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="268fc-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="268fc-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="268fc-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="268fc-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="268fc-119">Schema name</span></span>  <br/> |<span data-ttu-id="268fc-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="268fc-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="268fc-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="268fc-121">Validation file</span></span>  <br/> |<span data-ttu-id="268fc-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="268fc-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="268fc-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="268fc-123">Can be empty</span></span>  <br/> |<span data-ttu-id="268fc-124">False</span><span class="sxs-lookup"><span data-stu-id="268fc-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="268fc-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="268fc-125">See also</span></span>



[<span data-ttu-id="268fc-126">GetNonIndexableItemDetails-Vorgang</span><span class="sxs-lookup"><span data-stu-id="268fc-126">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)


- [<span data-ttu-id="268fc-127">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="268fc-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

