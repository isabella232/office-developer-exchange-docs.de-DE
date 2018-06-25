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
description: Das SerializedSecurityContext-Element wird in der Kopfzeile (SOAP = Simple Object Access Protocol) für tokenserialisierung für Server-zu-Server-Authentifizierung verwendet. Tokenserialisierung wird nicht unterstützt.
ms.openlocfilehash: c5590551dc0780d918b05902e4f48fb9d1390b59
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831363"
---
# <a name="serializedsecuritycontext"></a><span data-ttu-id="ca7ac-104">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="ca7ac-104">SerializedSecurityContext</span></span>

<span data-ttu-id="ca7ac-105">Das **SerializedSecurityContext** -Element wird in der Kopfzeile (SOAP = Simple Object Access Protocol) für tokenserialisierung für Server-zu-Server-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ca7ac-105">The **SerializedSecurityContext** element is used in the Simple Object Access Protocol (SOAP) header for token serialization in server-to-server authentication.</span></span> <span data-ttu-id="ca7ac-106">Tokenserialisierung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ca7ac-106">Token serialization is not supported.</span></span> 
  
```xml
<SerializedSecurityContext>
   <UserSid/>
   <GroupSids/>
   <RestrictedGroupSids/>
   <PrimarySmtpAddress/>
</SerializedSecurityContext>
```

 <span data-ttu-id="ca7ac-107">**SerializedSecurityContextType**</span><span class="sxs-lookup"><span data-stu-id="ca7ac-107">**SerializedSecurityContextType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ca7ac-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ca7ac-108">Attributes and elements</span></span>

<span data-ttu-id="ca7ac-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ca7ac-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ca7ac-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ca7ac-110">Attributes</span></span>

<span data-ttu-id="ca7ac-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ca7ac-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ca7ac-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ca7ac-112">Child elements</span></span>

|<span data-ttu-id="ca7ac-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ca7ac-113">**Element**</span></span>|<span data-ttu-id="ca7ac-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ca7ac-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ca7ac-115">UserSid</span><span class="sxs-lookup"><span data-stu-id="ca7ac-115">UserSid</span></span>](usersid.md) <br/> |<span data-ttu-id="ca7ac-116">Stellt die Security Descriptor Definition Language (SDDL) Formular der Benutzer Sicherheits-ID in einem serialisierten Sicherheit Kontext SOAP-Header.</span><span class="sxs-lookup"><span data-stu-id="ca7ac-116">Represents the security descriptor definition language (SDDL) form of the user security identifier in a serialized security context SOAP header.</span></span>  <br/> |
|[<span data-ttu-id="ca7ac-117">GroupSids</span><span class="sxs-lookup"><span data-stu-id="ca7ac-117">GroupSids</span></span>](groupsids.md) <br/> |<span data-ttu-id="ca7ac-118">Stellt eine Auflistung von Sicherheits-IDs von Active Directory Directory Service Group-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ca7ac-118">Represents a collection of Active Directory directory service group object security identifiers.</span></span>  <br/> |
|[<span data-ttu-id="ca7ac-119">RestrictedGroupSids</span><span class="sxs-lookup"><span data-stu-id="ca7ac-119">RestrictedGroupSids</span></span>](restrictedgroupsids.md) <br/> |<span data-ttu-id="ca7ac-120">Stellt die Gruppe Sicherheits-ID und die Attribute für eine eingeschränkte Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ca7ac-120">Represents the group security identifier and attributes for a restricted group.</span></span>  <br/> |
|[<span data-ttu-id="ca7ac-121">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="ca7ac-121">PrimarySmtpAddress</span></span>](primarysmtpaddress.md) <br/> |<span data-ttu-id="ca7ac-122">Stellt die primäre Simple Mail Transfer Protocol (SMTP)-Adresse eines Kontos für Server-zu-Server-Autorisierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca7ac-122">Represents the primary Simple Mail Transfer Protocol (SMTP) address of an account to be used for server-to-server authorization.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ca7ac-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ca7ac-123">Parent elements</span></span>

<span data-ttu-id="ca7ac-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="ca7ac-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ca7ac-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ca7ac-125">Remarks</span></span>

<span data-ttu-id="ca7ac-126">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2007 ausgeführt wird, die die Clientzugriffsserver (CAS) Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ca7ac-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server (CAS) role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ca7ac-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ca7ac-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca7ac-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="ca7ac-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ca7ac-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ca7ac-129">Schema Name</span></span>  <br/> |<span data-ttu-id="ca7ac-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ca7ac-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="ca7ac-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ca7ac-131">Validation File</span></span>  <br/> |<span data-ttu-id="ca7ac-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ca7ac-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ca7ac-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ca7ac-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="ca7ac-134">False</span><span class="sxs-lookup"><span data-stu-id="ca7ac-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ca7ac-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca7ac-135">See also</span></span>



- [<span data-ttu-id="ca7ac-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ca7ac-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="ca7ac-137">Server-zu-Server-Autorisierung in Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="ca7ac-137">Server-to-server authorization in EWS</span></span>](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

