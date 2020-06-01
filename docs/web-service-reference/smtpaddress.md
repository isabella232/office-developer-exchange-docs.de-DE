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
description: Das SmtpAddress-Element stellt die Simple Mail Transfer Protocol (SMTP) Adresse eines Kontos dar, das für den Identitätswechsel oder eine Simple Mail Transfer Protocol (SMTP) Empfängeradresse einer Kalender-oder Kontaktfreigabe Anforderung verwendet werden soll.
ms.openlocfilehash: 915ff328cc384c1f2884e9fbea8c10c1ebc79288
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466689"
---
# <a name="smtpaddress"></a><span data-ttu-id="ad0d2-103">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="ad0d2-103">SmtpAddress</span></span>

<span data-ttu-id="ad0d2-104">Das **SmtpAddress** -Element stellt die Simple Mail Transfer Protocol (SMTP) Adresse eines Kontos dar, das für den Identitätswechsel oder eine Simple Mail Transfer Protocol (SMTP) Empfängeradresse einer Kalender-oder Kontaktfreigabe Anforderung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad0d2-104">The **SmtpAddress** element represents the Simple Mail Transfer Protocol (SMTP) address of an account to be used for impersonation or a Simple Mail Transfer Protocol (SMTP) recipient address of a calendar or contact sharing request.</span></span> 
  
```xml
<SmtpAddress/>
```

<span data-ttu-id="ad0d2-105">**SmtpAddressType**</span><span class="sxs-lookup"><span data-stu-id="ad0d2-105">**SmtpAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ad0d2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ad0d2-106">Attributes and elements</span></span>

<span data-ttu-id="ad0d2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ad0d2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad0d2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ad0d2-108">Attributes</span></span>

<span data-ttu-id="ad0d2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ad0d2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ad0d2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad0d2-110">Child elements</span></span>

<span data-ttu-id="ad0d2-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ad0d2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ad0d2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad0d2-112">Parent elements</span></span>

|<span data-ttu-id="ad0d2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad0d2-113">**Element**</span></span>|<span data-ttu-id="ad0d2-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad0d2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad0d2-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="ad0d2-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="ad0d2-116">Stellt ein Konto für den Identitätswechsel dar, wenn Sie den SOAP-ExchangeImpersonation-Header verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad0d2-116">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="ad0d2-117">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="ad0d2-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[<span data-ttu-id="ad0d2-118">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="ad0d2-118">InvalidRecipient</span></span>](invalidrecipient.md) <br/> |<span data-ttu-id="ad0d2-119">Stellt einen ungültigen Empfänger für eine Kalenderfreigabe-oder Kontaktfreigabe Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="ad0d2-119">Represents an invalid recipient for a calendar sharing or contact sharing message.</span></span>  <br/> |
|[<span data-ttu-id="ad0d2-120">Recipients (ArrayOfSmtpAddressType)</span><span class="sxs-lookup"><span data-stu-id="ad0d2-120">Recipients (ArrayOfSmtpAddressType)</span></span>](recipients-arrayofsmtpaddresstype.md) <br/> |<span data-ttu-id="ad0d2-121">Stellt eine Auflistung von Empfängern dar, denen Zugriff auf den freigegebenen Ordner gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="ad0d2-121">Represents a collection of recipients that will be granted access to the shared folder.</span></span>  <br/> |
|[<span data-ttu-id="ad0d2-122">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="ad0d2-122">GetSharingFolder</span></span>](getsharingfolder.md) <br/> |<span data-ttu-id="ad0d2-123">Definiert eine Anforderung zum Abrufen der lokalen Ordner-ID eines angegebenen freigegebenen Ordners.</span><span class="sxs-lookup"><span data-stu-id="ad0d2-123">Defines a request to get the local folder identifier of a specified shared folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ad0d2-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="ad0d2-124">Text value</span></span>

<span data-ttu-id="ad0d2-125">Ein Textwert, der eine SMTP-Adresse darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ad0d2-125">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ad0d2-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad0d2-126">Remarks</span></span>

<span data-ttu-id="ad0d2-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste des Computers gehostet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ad0d2-127">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad0d2-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ad0d2-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad0d2-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad0d2-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ad0d2-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ad0d2-130">Schema Name</span></span>  <br/> |<span data-ttu-id="ad0d2-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ad0d2-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="ad0d2-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ad0d2-132">Validation File</span></span>  <br/> |<span data-ttu-id="ad0d2-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ad0d2-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ad0d2-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ad0d2-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="ad0d2-135">False</span><span class="sxs-lookup"><span data-stu-id="ad0d2-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad0d2-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad0d2-136">See also</span></span>

- [<span data-ttu-id="ad0d2-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ad0d2-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

