---
title: InPlaceHoldIdentity
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54f45774-00a0-4392-af1b-8c5f2208a53f
description: Das InPlaceHoldIdentity-Element gibt die Identität eines Haltestatus an, der die Postfachelemente beibehält.
ms.openlocfilehash: a06f72e478e7dc5bd1a499dceefeb352b14d7362
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466094"
---
# <a name="inplaceholdidentity"></a><span data-ttu-id="61954-103">InPlaceHoldIdentity</span><span class="sxs-lookup"><span data-stu-id="61954-103">InPlaceHoldIdentity</span></span>

<span data-ttu-id="61954-104">Das **InPlaceHoldIdentity** -Element gibt die Identität eines Haltestatus an, der die Postfachelemente beibehält.</span><span class="sxs-lookup"><span data-stu-id="61954-104">The **InPlaceHoldIdentity** element specifies the identity of a hold that preserves the mailbox items.</span></span> 
  
```XML
<InPlaceHoldIdentity></InPlaceHoldIdentity>
```

 <span data-ttu-id="61954-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="61954-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="61954-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="61954-106">Attributes and elements</span></span>

<span data-ttu-id="61954-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="61954-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61954-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="61954-108">Attributes</span></span>

<span data-ttu-id="61954-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="61954-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="61954-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61954-110">Child elements</span></span>

<span data-ttu-id="61954-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="61954-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="61954-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61954-112">Parent elements</span></span>

<span data-ttu-id="61954-113">[SetHoldOnMailboxes](setholdonmailboxes.md)  |  [DiscoverySearchConfiguration](discoverysearchconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="61954-113">[SetHoldOnMailboxes](setholdonmailboxes.md) | [DiscoverySearchConfiguration](discoverysearchconfiguration.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="61954-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="61954-114">Text value</span></span>

<span data-ttu-id="61954-115">Der Textwert des **InPlaceHoldIdentity** -Elements ist die Mailbox-halte-ID.</span><span class="sxs-lookup"><span data-stu-id="61954-115">The text value of the **InPlaceHoldIdentity** element is the mailbox hold identifier.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="61954-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61954-116">Remarks</span></span>

<span data-ttu-id="61954-117">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="61954-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="61954-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="61954-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61954-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="61954-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61954-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="61954-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="61954-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="61954-121">Schema name</span></span>  <br/> |<span data-ttu-id="61954-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="61954-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="61954-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="61954-123">Validation file</span></span>  <br/> |<span data-ttu-id="61954-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="61954-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="61954-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="61954-125">Can be empty</span></span>  <br/> |<span data-ttu-id="61954-126">False</span><span class="sxs-lookup"><span data-stu-id="61954-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="61954-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61954-127">See also</span></span>



[<span data-ttu-id="61954-128">SetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="61954-128">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)


- [<span data-ttu-id="61954-129">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="61954-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

