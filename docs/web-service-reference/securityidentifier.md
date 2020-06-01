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
description: Das SecurityIdentifier-Element stellt das SDDL-Formular (Security Descriptor Definition Language) einer Sicherheits-ID (Security Identifier, SID) dar.
ms.openlocfilehash: c55e4a7f7f0b8f8a40e6fcaf8d18e253a6da2679
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468803"
---
# <a name="securityidentifier"></a><span data-ttu-id="4c3dd-103">SecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="4c3dd-103">SecurityIdentifier</span></span>

<span data-ttu-id="4c3dd-104">Das **SecurityIdentifier** -Element stellt das SDDL-Formular (Security Descriptor Definition Language) einer Sicherheits-ID (Security Identifier, [sid](sid.md)) dar.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-104">The **SecurityIdentifier** element represents the security descriptor definition language (SDDL) form of a security identifier ( [SID](sid.md)).</span></span>
  
```xml
<SecurityIdentifier/>
```

 <span data-ttu-id="4c3dd-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4c3dd-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4c3dd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4c3dd-106">Attributes and elements</span></span>

<span data-ttu-id="4c3dd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4c3dd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4c3dd-108">Attributes</span></span>

<span data-ttu-id="4c3dd-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4c3dd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4c3dd-110">Child elements</span></span>

<span data-ttu-id="4c3dd-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4c3dd-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4c3dd-112">Parent elements</span></span>

|<span data-ttu-id="4c3dd-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4c3dd-113">**Element**</span></span>|<span data-ttu-id="4c3dd-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4c3dd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4c3dd-115">GroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="4c3dd-115">GroupIdentifier</span></span>](groupidentifier.md) <br/> |<span data-ttu-id="4c3dd-116">Stellt eine einzelne Sicherheits-ID und ein einzelnes Attribut für eine Active Directory Objektgruppe dar, der das Konto angehört.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-116">Represents a single security identifier and attribute for an Active Directory object group of which the account is a member.</span></span>  <br/> <span data-ttu-id="4c3dd-117">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="4c3dd-117">The following is the XPath expression to this element:</span></span>  <br/>  `/SerializedSecurityContext/GroupSids/GroupIdentifier[i]` <br/> |
|[<span data-ttu-id="4c3dd-118">RestrictedGroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="4c3dd-118">RestrictedGroupIdentifier</span></span>](restrictedgroupidentifier.md) <br/> |<span data-ttu-id="4c3dd-119">Stellt die Gruppen Sicherheits-ID und die Attribute für eine eingeschränkte Gruppe in einem Benutzertoken dar.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-119">Represents the group security identifier and attributes for a restricted group within a user token.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c3dd-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c3dd-120">Remarks</span></span>

<span data-ttu-id="4c3dd-121">Dieses Element wird im Simple Object Access Protocol (SOAP)-Header verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-121">This element is used in the Simple Object Access Protocol (SOAP) header.</span></span>
  
<span data-ttu-id="4c3dd-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="4c3dd-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4c3dd-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4c3dd-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c3dd-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="4c3dd-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4c3dd-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4c3dd-125">Schema Name</span></span>  <br/> |<span data-ttu-id="4c3dd-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4c3dd-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="4c3dd-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4c3dd-127">Validation File</span></span>  <br/> |<span data-ttu-id="4c3dd-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4c3dd-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4c3dd-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4c3dd-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="4c3dd-130">False</span><span class="sxs-lookup"><span data-stu-id="4c3dd-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4c3dd-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c3dd-131">See also</span></span>



- [<span data-ttu-id="4c3dd-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4c3dd-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

