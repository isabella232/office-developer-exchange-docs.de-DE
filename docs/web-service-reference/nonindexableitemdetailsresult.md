---
title: NonIndexableItemDetailsResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7cbdbc21-5405-4cbc-8ca0-d7b0257927aa
description: Das NonIndexableItemDetailsResult-Element gibt die Ergebnisse des GetNonIndexableItemDetails-WSDL-Vorgangs an.
ms.openlocfilehash: 647f58b5e7285af70bbfb3a203ba71c9a3ccebcc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465443"
---
# <a name="nonindexableitemdetailsresult"></a><span data-ttu-id="53ca8-103">NonIndexableItemDetailsResult</span><span class="sxs-lookup"><span data-stu-id="53ca8-103">NonIndexableItemDetailsResult</span></span>

<span data-ttu-id="53ca8-104">Das **NonIndexableItemDetailsResult** -Element gibt die Ergebnisse des **GetNonIndexableItemDetails** -WSDL-Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="53ca8-104">The **NonIndexableItemDetailsResult** element specifies the results of the **GetNonIndexableItemDetails** WSDL operation.</span></span> 
  
```XML
<NonIndexableItemDetailsResult>
   <Items/>
   <FailedMailboxes/>
</NonIndexableItemDetailsResult>
```

 <span data-ttu-id="53ca8-105">**NonIndexableItemDetailResultType**</span><span class="sxs-lookup"><span data-stu-id="53ca8-105">**NonIndexableItemDetailResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="53ca8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="53ca8-106">Attributes and elements</span></span>

<span data-ttu-id="53ca8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="53ca8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53ca8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="53ca8-108">Attributes</span></span>

<span data-ttu-id="53ca8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="53ca8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="53ca8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="53ca8-110">Child elements</span></span>

<span data-ttu-id="53ca8-111">[Items (ArrayOfNonIndexableItemDetailsType)](items-arrayofnonindexableitemdetailstype.md) , [FailedMailboxes](failedmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="53ca8-111">[Items (ArrayOfNonIndexableItemDetailsType)](items-arrayofnonindexableitemdetailstype.md) , [FailedMailboxes](failedmailboxes.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="53ca8-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="53ca8-112">Parent elements</span></span>

<span data-ttu-id="53ca8-113">[GetNonIndexableItemDetailsResponse](getnonindexableitemdetailsresponse.md) , [GetNonIndexableItemDetailsResponseMessage](getnonindexableitemdetailsresponsemessage.md)</span><span class="sxs-lookup"><span data-stu-id="53ca8-113">[GetNonIndexableItemDetailsResponse](getnonindexableitemdetailsresponse.md) , [GetNonIndexableItemDetailsResponseMessage](getnonindexableitemdetailsresponsemessage.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="53ca8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53ca8-114">Remarks</span></span>

<span data-ttu-id="53ca8-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="53ca8-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="53ca8-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="53ca8-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="53ca8-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="53ca8-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53ca8-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="53ca8-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="53ca8-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="53ca8-119">Schema name</span></span>  <br/> |<span data-ttu-id="53ca8-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="53ca8-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="53ca8-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="53ca8-121">Validation file</span></span>  <br/> |<span data-ttu-id="53ca8-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="53ca8-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="53ca8-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="53ca8-123">Can be empty</span></span>  <br/> |<span data-ttu-id="53ca8-124">False</span><span class="sxs-lookup"><span data-stu-id="53ca8-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53ca8-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53ca8-125">See also</span></span>



[<span data-ttu-id="53ca8-126">GetNonIndexableItemDetails-Vorgang</span><span class="sxs-lookup"><span data-stu-id="53ca8-126">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)


- [<span data-ttu-id="53ca8-127">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="53ca8-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

