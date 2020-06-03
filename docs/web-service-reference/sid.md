---
title: SID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SID
api_type:
- schema
ms.assetid: 2f33b29b-163b-4106-a74d-6fb76ec38951
description: Das sid-Element stellt das SDDL-Formular (Security Descriptor Definition Language) der Sicherheits-ID (Security Identifier, SID) für das Konto dar, das für den Identitätswechsel oder den Stellvertretungszugriff verwendet werden soll.
ms.openlocfilehash: 0e3f740e9a056f7c0042049d97757b5f2d3c441d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468047"
---
# <a name="sid"></a><span data-ttu-id="cf570-103">SID</span><span class="sxs-lookup"><span data-stu-id="cf570-103">SID</span></span>

<span data-ttu-id="cf570-104">Das **sid** -Element stellt das SDDL-Formular (Security Descriptor Definition Language) der Sicherheits-ID (Security Identifier, SID) für das Konto dar, das für den Identitätswechsel oder den Stellvertretungszugriff verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf570-104">The **SID** element represents the security descriptor definition language (SDDL) form of the security identifier (SID) for the account to use for impersonation or delegate access.</span></span> 
  
```xml
<SID/>
```

 <span data-ttu-id="cf570-105">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="cf570-105">**SIDType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cf570-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cf570-106">Attributes and elements</span></span>

<span data-ttu-id="cf570-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cf570-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf570-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cf570-108">Attributes</span></span>

<span data-ttu-id="cf570-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="cf570-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cf570-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cf570-110">Child elements</span></span>

<span data-ttu-id="cf570-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="cf570-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cf570-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cf570-112">Parent elements</span></span>

|<span data-ttu-id="cf570-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="cf570-113">**Element**</span></span>|<span data-ttu-id="cf570-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cf570-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf570-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="cf570-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="cf570-116">Stellt ein Konto für den Identitätswechsel dar, wenn der ExchangeImpersonation-SOAP-Header verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf570-116">Represents an account to impersonate when using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="cf570-117">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="cf570-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[<span data-ttu-id="cf570-118">UserId</span><span class="sxs-lookup"><span data-stu-id="cf570-118">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="cf570-119">Identifiziert einen Stellvertreter Benutzer oder einen Benutzer mit Ordnerzugriffsberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="cf570-119">Identifies a delegate user or a user with folder access permissions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cf570-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="cf570-120">Text value</span></span>

<span data-ttu-id="cf570-121">Der Wert Text ist eine Zeichenfolgendarstellung einer SID.</span><span class="sxs-lookup"><span data-stu-id="cf570-121">The text value is a string representation of a SID.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cf570-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf570-122">Remarks</span></span>

<span data-ttu-id="cf570-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server mit installierter Client Zugriffs-Server Rolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="cf570-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cf570-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="cf570-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf570-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="cf570-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cf570-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cf570-126">Schema Name</span></span>  <br/> |<span data-ttu-id="cf570-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="cf570-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="cf570-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cf570-128">Validation File</span></span>  <br/> |<span data-ttu-id="cf570-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cf570-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cf570-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="cf570-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="cf570-131">False</span><span class="sxs-lookup"><span data-stu-id="cf570-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf570-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf570-132">See also</span></span>



- [<span data-ttu-id="cf570-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cf570-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

