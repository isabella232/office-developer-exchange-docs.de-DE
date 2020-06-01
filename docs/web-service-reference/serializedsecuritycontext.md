---
title: SerializedSecurityContext
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SerializedSecurityContext
api_type:
- schema
ms.assetid: a02c4fc1-ed1a-40d9-a18e-6cfdae21a690
description: Das SerializedSecurityContext-Element wird in der Simple Object Access Protocol (SOAP) Kopfzeile für die Token-Serialisierung in der Server-zu-Server-Authentifizierung verwendet. Die Serialisierung von Token wird nicht unterstützt.
ms.openlocfilehash: 58fea1c7f613315d59e81935561f92f318afc769
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462052"
---
# <a name="serializedsecuritycontext"></a><span data-ttu-id="4e1e6-104">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="4e1e6-104">SerializedSecurityContext</span></span>

<span data-ttu-id="4e1e6-105">Das **SerializedSecurityContext** -Element wird in der Simple Object Access Protocol (SOAP) Kopfzeile für die Token-Serialisierung in der Server-zu-Server-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="4e1e6-105">The **SerializedSecurityContext** element is used in the Simple Object Access Protocol (SOAP) header for token serialization in server-to-server authentication.</span></span> <span data-ttu-id="4e1e6-106">Die Serialisierung von Token wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4e1e6-106">Token serialization is not supported.</span></span> 
  
```xml
<SerializedSecurityContext>
   <UserSid/>
   <GroupSids/>
   <RestrictedGroupSids/>
   <PrimarySmtpAddress/>
</SerializedSecurityContext>
```

 <span data-ttu-id="4e1e6-107">**SerializedSecurityContextType**</span><span class="sxs-lookup"><span data-stu-id="4e1e6-107">**SerializedSecurityContextType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4e1e6-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4e1e6-108">Attributes and elements</span></span>

<span data-ttu-id="4e1e6-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4e1e6-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4e1e6-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="4e1e6-110">Attributes</span></span>

<span data-ttu-id="4e1e6-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="4e1e6-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4e1e6-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4e1e6-112">Child elements</span></span>

|<span data-ttu-id="4e1e6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4e1e6-113">**Element**</span></span>|<span data-ttu-id="4e1e6-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4e1e6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e1e6-115">UserSID</span><span class="sxs-lookup"><span data-stu-id="4e1e6-115">UserSid</span></span>](usersid.md) <br/> |<span data-ttu-id="4e1e6-116">Stellt das SDDL-Formular (Security Descriptor Definition Language) der Benutzer Sicherheits-ID in einem serialisierten Sicherheitskontext-SOAP-Header dar.</span><span class="sxs-lookup"><span data-stu-id="4e1e6-116">Represents the security descriptor definition language (SDDL) form of the user security identifier in a serialized security context SOAP header.</span></span>  <br/> |
|[<span data-ttu-id="4e1e6-117">GroupSids</span><span class="sxs-lookup"><span data-stu-id="4e1e6-117">GroupSids</span></span>](groupsids.md) <br/> |<span data-ttu-id="4e1e6-118">Stellt eine Auflistung von Sicherheits-IDs für das Verzeichnisdienst-Gruppenobjekt Active Directory dar.</span><span class="sxs-lookup"><span data-stu-id="4e1e6-118">Represents a collection of Active Directory directory service group object security identifiers.</span></span>  <br/> |
|[<span data-ttu-id="4e1e6-119">RestrictedGroupSids</span><span class="sxs-lookup"><span data-stu-id="4e1e6-119">RestrictedGroupSids</span></span>](restrictedgroupsids.md) <br/> |<span data-ttu-id="4e1e6-120">Stellt die Gruppen Sicherheits-ID und die Attribute für eine eingeschränkte Gruppe dar.</span><span class="sxs-lookup"><span data-stu-id="4e1e6-120">Represents the group security identifier and attributes for a restricted group.</span></span>  <br/> |
|[<span data-ttu-id="4e1e6-121">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="4e1e6-121">PrimarySmtpAddress</span></span>](primarysmtpaddress.md) <br/> |<span data-ttu-id="4e1e6-122">Stellt die primäre Simple Mail Transfer Protocol (SMTP) Adresse eines Kontos dar, das für die Server-zu-Server-Autorisierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4e1e6-122">Represents the primary Simple Mail Transfer Protocol (SMTP) address of an account to be used for server-to-server authorization.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4e1e6-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4e1e6-123">Parent elements</span></span>

<span data-ttu-id="4e1e6-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="4e1e6-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4e1e6-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e1e6-125">Remarks</span></span>

<span data-ttu-id="4e1e6-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs Server-Rolle (CAS) installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4e1e6-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server (CAS) role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4e1e6-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4e1e6-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e1e6-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="4e1e6-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4e1e6-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4e1e6-129">Schema Name</span></span>  <br/> |<span data-ttu-id="4e1e6-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4e1e6-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="4e1e6-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4e1e6-131">Validation File</span></span>  <br/> |<span data-ttu-id="4e1e6-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4e1e6-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4e1e6-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4e1e6-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="4e1e6-134">False</span><span class="sxs-lookup"><span data-stu-id="4e1e6-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4e1e6-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e1e6-135">See also</span></span>



- [<span data-ttu-id="4e1e6-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4e1e6-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="4e1e6-137">Server-zu-Server-Autorisierung in EWS</span><span class="sxs-lookup"><span data-stu-id="4e1e6-137">Server-to-server authorization in EWS</span></span>](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

