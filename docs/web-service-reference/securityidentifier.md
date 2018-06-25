---
title: SecurityIdentifier
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SecurityIdentifier
api_type:
- schema
ms.assetid: f7656729-f2c9-41cc-b1ec-60f480fc4dab
description: Das Element SecurityIdentifier stellt Security Descriptor Definition Language (SDDL) Form einer Sicherheits-ID (SID).
ms.openlocfilehash: c18d7d4505c618792497c32c7499eab9ac82989e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831314"
---
# <a name="securityidentifier"></a><span data-ttu-id="a40f3-103">SecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="a40f3-103">SecurityIdentifier</span></span>

<span data-ttu-id="a40f3-104">Das Element **SecurityIdentifier** stellt Security Descriptor Definition Language (SDDL) Form einer Sicherheits-ID ( [SID](sid.md)).</span><span class="sxs-lookup"><span data-stu-id="a40f3-104">The **SecurityIdentifier** element represents the security descriptor definition language (SDDL) form of a security identifier ( [SID](sid.md)).</span></span>
  
```xml
<SecurityIdentifier/>
```

 <span data-ttu-id="a40f3-105">**string**</span><span class="sxs-lookup"><span data-stu-id="a40f3-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a40f3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a40f3-106">Attributes and elements</span></span>

<span data-ttu-id="a40f3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a40f3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a40f3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a40f3-108">Attributes</span></span>

<span data-ttu-id="a40f3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a40f3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a40f3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a40f3-110">Child elements</span></span>

<span data-ttu-id="a40f3-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="a40f3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a40f3-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a40f3-112">Parent elements</span></span>

|<span data-ttu-id="a40f3-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a40f3-113">**Element**</span></span>|<span data-ttu-id="a40f3-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a40f3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a40f3-115">GroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="a40f3-115">GroupIdentifier</span></span>](groupidentifier.md) <br/> |<span data-ttu-id="a40f3-116">Stellt eine einzelne Sicherheits-ID und das Attribut für eine Active Directory-Gruppe, Objekt, das Konto ein Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="a40f3-116">Represents a single security identifier and attribute for an Active Directory object group of which the account is a member.</span></span>  <br/> <span data-ttu-id="a40f3-117">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="a40f3-117">The following is the XPath expression to this element:</span></span>  <br/>  `/SerializedSecurityContext/GroupSids/GroupIdentifier[i]` <br/> |
|[<span data-ttu-id="a40f3-118">RestrictedGroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="a40f3-118">RestrictedGroupIdentifier</span></span>](restrictedgroupidentifier.md) <br/> |<span data-ttu-id="a40f3-119">Stellt die Gruppe Sicherheits-ID und die Attribute für eine eingeschränkte Gruppe innerhalb einer Benutzertoken.</span><span class="sxs-lookup"><span data-stu-id="a40f3-119">Represents the group security identifier and attributes for a restricted group within a user token.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a40f3-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a40f3-120">Remarks</span></span>

<span data-ttu-id="a40f3-121">Dieses Element wird in der Kopfzeile (SOAP = Simple Object Access Protocol) verwendet.</span><span class="sxs-lookup"><span data-stu-id="a40f3-121">This element is used in the Simple Object Access Protocol (SOAP) header.</span></span>
  
<span data-ttu-id="a40f3-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a40f3-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a40f3-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a40f3-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a40f3-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="a40f3-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a40f3-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a40f3-125">Schema Name</span></span>  <br/> |<span data-ttu-id="a40f3-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a40f3-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="a40f3-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a40f3-127">Validation File</span></span>  <br/> |<span data-ttu-id="a40f3-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a40f3-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a40f3-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a40f3-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="a40f3-130">False</span><span class="sxs-lookup"><span data-stu-id="a40f3-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a40f3-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a40f3-131">See also</span></span>



- [<span data-ttu-id="a40f3-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a40f3-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

