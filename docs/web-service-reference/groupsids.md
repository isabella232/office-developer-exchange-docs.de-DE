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
description: Das Element GroupSids stellt eine Sammlung von Sicherheits-IDs von Active Directory Directory Service Group-Objekt.
ms.openlocfilehash: c24c8ea3c3b7d37f41986997ed924c951b4a48ef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829790"
---
# <a name="groupsids"></a><span data-ttu-id="9fedb-103">GroupSids</span><span class="sxs-lookup"><span data-stu-id="9fedb-103">GroupSids</span></span>

<span data-ttu-id="9fedb-104">Das Element **GroupSids** stellt eine Sammlung von Sicherheits-IDs von Active Directory Directory Service Group-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9fedb-104">The **GroupSids** element represents a collection of Active Directory directory service group object security identifiers.</span></span> 
  
```xml
<GroupSids>
   <GroupIdentifier/>
</GroupSids>
```

 <span data-ttu-id="9fedb-105">**NonEmptyArrayOfGroupIdentifiersType**</span><span class="sxs-lookup"><span data-stu-id="9fedb-105">**NonEmptyArrayOfGroupIdentifiersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9fedb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9fedb-106">Attributes and elements</span></span>

<span data-ttu-id="9fedb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9fedb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9fedb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9fedb-108">Attributes</span></span>

<span data-ttu-id="9fedb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9fedb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9fedb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9fedb-110">Child elements</span></span>

|<span data-ttu-id="9fedb-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9fedb-111">**Element**</span></span>|<span data-ttu-id="9fedb-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9fedb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9fedb-113">GroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="9fedb-113">GroupIdentifier</span></span>](groupidentifier.md) <br/> |<span data-ttu-id="9fedb-114">Stellt eine einzelne Sicherheits-ID und das Attribut für eine Active Directory-Gruppe, Objekt, das Konto ein Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="9fedb-114">Represents a single security identifier and attribute for an Active Directory object group of which the account is a member.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9fedb-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9fedb-115">Parent elements</span></span>

|<span data-ttu-id="9fedb-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="9fedb-116">**Element**</span></span>|<span data-ttu-id="9fedb-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9fedb-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9fedb-118">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="9fedb-118">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="9fedb-119">Wird in der Kopfzeile (SOAP = Simple Object Access Protocol) für tokenserialisierung für Server-zu-Server-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9fedb-119">Used in the Simple Object Access Protocol (SOAP) header for token serialization in server-to-server authentication.</span></span> <span data-ttu-id="9fedb-120">Tokenserialisierung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9fedb-120">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fedb-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9fedb-121">Remarks</span></span>

<span data-ttu-id="9fedb-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="9fedb-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9fedb-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9fedb-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fedb-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="9fedb-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9fedb-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9fedb-125">Schema Name</span></span>  <br/> |<span data-ttu-id="9fedb-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9fedb-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="9fedb-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9fedb-127">Validation File</span></span>  <br/> |<span data-ttu-id="9fedb-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9fedb-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9fedb-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9fedb-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="9fedb-130">False</span><span class="sxs-lookup"><span data-stu-id="9fedb-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9fedb-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fedb-131">See also</span></span>



- [<span data-ttu-id="9fedb-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9fedb-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

