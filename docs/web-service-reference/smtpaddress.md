---
title: SmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SmtpAddress
api_type:
- schema
ms.assetid: 779305a6-ad1e-424e-8a69-4e3bef61d787
description: SmtpAddress-Element stellt die Simple Mail Transfer Protocol (SMTP)-Adresse eines Kontos für den Identitätswechsel verwendet werden oder Simple Mail Transfer Protocol (SMTP) Empfängeradresse eines Kalenders oder Kontakt Freigabeanfrage dar.
ms.openlocfilehash: 39588f0892cdcec819a1972547155730be5785f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831511"
---
# <a name="smtpaddress"></a><span data-ttu-id="5f521-103">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="5f521-103">SmtpAddress</span></span>

<span data-ttu-id="5f521-104">**SmtpAddress** -Element stellt die Simple Mail Transfer Protocol (SMTP)-Adresse eines Kontos für den Identitätswechsel verwendet werden oder Simple Mail Transfer Protocol (SMTP) Empfängeradresse eines Kalenders oder Kontakt Freigabeanfrage dar.</span><span class="sxs-lookup"><span data-stu-id="5f521-104">The **SmtpAddress** element represents the Simple Mail Transfer Protocol (SMTP) address of an account to be used for impersonation or a Simple Mail Transfer Protocol (SMTP) recipient address of a calendar or contact sharing request.</span></span> 
  
```xml
<SmtpAddress/>
```

<span data-ttu-id="5f521-105">**SmtpAddressType**</span><span class="sxs-lookup"><span data-stu-id="5f521-105">**SmtpAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5f521-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5f521-106">Attributes and elements</span></span>

<span data-ttu-id="5f521-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5f521-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f521-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5f521-108">Attributes</span></span>

<span data-ttu-id="5f521-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5f521-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5f521-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5f521-110">Child elements</span></span>

<span data-ttu-id="5f521-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5f521-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5f521-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5f521-112">Parent elements</span></span>

|<span data-ttu-id="5f521-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5f521-113">**Element**</span></span>|<span data-ttu-id="5f521-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5f521-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f521-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="5f521-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="5f521-116">Gibt ein Konto Identitätswechsel bei Verwendung der "ExchangeImpersonation" SOAP-Header.</span><span class="sxs-lookup"><span data-stu-id="5f521-116">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="5f521-117">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="5f521-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[<span data-ttu-id="5f521-118">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="5f521-118">InvalidRecipient</span></span>](invalidrecipient.md) <br/> |<span data-ttu-id="5f521-119">Stellt einen ungültigen Empfänger für einen zum Freigeben von Kalendern oder Kontakt Freigabenachricht an.</span><span class="sxs-lookup"><span data-stu-id="5f521-119">Represents an invalid recipient for a calendar sharing or contact sharing message.</span></span>  <br/> |
|[<span data-ttu-id="5f521-120">Empfänger (ArrayOfSmtpAddressType)</span><span class="sxs-lookup"><span data-stu-id="5f521-120">Recipients (ArrayOfSmtpAddressType)</span></span>](recipients-arrayofsmtpaddresstype.md) <br/> |<span data-ttu-id="5f521-121">Stellt eine Sammlung von Empfängern, die Zugriff auf den freigegebenen Ordner gewährt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f521-121">Represents a collection of recipients that will be granted access to the shared folder.</span></span>  <br/> |
|[<span data-ttu-id="5f521-122">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="5f521-122">GetSharingFolder</span></span>](getsharingfolder.md) <br/> |<span data-ttu-id="5f521-123">Definiert eine Anforderung an den lokalen Ordner Bezeichner eines angegebenen freigegebenen Ordners abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5f521-123">Defines a request to get the local folder identifier of a specified shared folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5f521-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="5f521-124">Text value</span></span>

<span data-ttu-id="5f521-125">Ein Textwert, der eine SMTP-Adresse darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5f521-125">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f521-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5f521-126">Remarks</span></span>

<span data-ttu-id="5f521-127">Das Schema, das dieses Element beschreibt befindet sich das virtuelle IIS-Verzeichnis, dass Hosts Exchange-Webdienste des Computers, auf dem Microsoft Exchange Server ausgeführt wird die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5f521-127">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5f521-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5f521-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f521-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f521-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5f521-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5f521-130">Schema Name</span></span>  <br/> |<span data-ttu-id="5f521-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5f521-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="5f521-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5f521-132">Validation File</span></span>  <br/> |<span data-ttu-id="5f521-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5f521-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5f521-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5f521-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="5f521-135">False</span><span class="sxs-lookup"><span data-stu-id="5f521-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5f521-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f521-136">See also</span></span>

- [<span data-ttu-id="5f521-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5f521-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

