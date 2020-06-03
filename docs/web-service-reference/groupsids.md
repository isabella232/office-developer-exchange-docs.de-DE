---
title: GroupSids
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupSids
api_type:
- schema
ms.assetid: ebb00653-83f0-4080-a902-c38df6719800
description: Das GroupSids-Element stellt eine Auflistung von Sicherheits-IDs für das Verzeichnisdienst-Gruppenobjekt Active Directory dar.
ms.openlocfilehash: 40f36176fcaa3e2160237f269fb2dc3b12bf8af2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530064"
---
# <a name="groupsids"></a><span data-ttu-id="d8241-103">GroupSids</span><span class="sxs-lookup"><span data-stu-id="d8241-103">GroupSids</span></span>

<span data-ttu-id="d8241-104">Das **GroupSids** -Element stellt eine Auflistung von Sicherheits-IDs für das Verzeichnisdienst-Gruppenobjekt Active Directory dar.</span><span class="sxs-lookup"><span data-stu-id="d8241-104">The **GroupSids** element represents a collection of Active Directory directory service group object security identifiers.</span></span> 
  
```xml
<GroupSids>
   <GroupIdentifier/>
</GroupSids>
```

 <span data-ttu-id="d8241-105">**NonEmptyArrayOfGroupIdentifiersType**</span><span class="sxs-lookup"><span data-stu-id="d8241-105">**NonEmptyArrayOfGroupIdentifiersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d8241-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d8241-106">Attributes and elements</span></span>

<span data-ttu-id="d8241-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d8241-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d8241-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d8241-108">Attributes</span></span>

<span data-ttu-id="d8241-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d8241-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d8241-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d8241-110">Child elements</span></span>

|<span data-ttu-id="d8241-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d8241-111">**Element**</span></span>|<span data-ttu-id="d8241-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d8241-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d8241-113">GroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="d8241-113">GroupIdentifier</span></span>](groupidentifier.md) <br/> |<span data-ttu-id="d8241-114">Stellt eine einzelne Sicherheits-ID und ein einzelnes Attribut für eine Active Directory Objektgruppe dar, der das Konto angehört.</span><span class="sxs-lookup"><span data-stu-id="d8241-114">Represents a single security identifier and attribute for an Active Directory object group of which the account is a member.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d8241-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d8241-115">Parent elements</span></span>

|<span data-ttu-id="d8241-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d8241-116">**Element**</span></span>|<span data-ttu-id="d8241-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d8241-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d8241-118">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="d8241-118">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="d8241-119">Wird im Simple Object Access Protocol (SOAP)-Header für die Token-Serialisierung in der Server-zu-Server-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8241-119">Used in the Simple Object Access Protocol (SOAP) header for token serialization in server-to-server authentication.</span></span> <span data-ttu-id="d8241-120">Die Serialisierung von Token wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d8241-120">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8241-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8241-121">Remarks</span></span>

<span data-ttu-id="d8241-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d8241-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d8241-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d8241-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8241-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="d8241-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d8241-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d8241-125">Schema Name</span></span>  <br/> |<span data-ttu-id="d8241-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d8241-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="d8241-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d8241-127">Validation File</span></span>  <br/> |<span data-ttu-id="d8241-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d8241-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d8241-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d8241-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="d8241-130">False</span><span class="sxs-lookup"><span data-stu-id="d8241-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d8241-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8241-131">See also</span></span>



- [<span data-ttu-id="d8241-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d8241-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

