---
title: Überprüfen eines Zertifikats für die EWS Managed API
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1fe0b215-8340-4bc8-a6ce-4f591ca9e353
description: Informationen Sie zum Erstellen und verweisen auf ein Zertifikat Validierung Rückrufmethode, damit Sie EWS Managed API-Anforderungen für einen Exchange-Server machen können.
ms.openlocfilehash: 13d7c51e55308b9e9997697a075c8a9e6b4f10d0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757009"
---
# <a name="validate-a-server-certificate-for-the-ews-managed-api"></a><span data-ttu-id="e7efe-103">Überprüfen eines Zertifikats für die EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="e7efe-103">Validate a server certificate for the EWS Managed API</span></span>

<span data-ttu-id="e7efe-104">Informationen Sie zum Erstellen und verweisen auf ein Zertifikat Validierung Rückrufmethode, damit Sie EWS Managed API-Anforderungen für einen Exchange-Server machen können.</span><span class="sxs-lookup"><span data-stu-id="e7efe-104">Learn how to create and reference a certificate validation callback method so that you can make EWS Managed API requests to an Exchange server.</span></span>
  
<span data-ttu-id="e7efe-105">Standardmäßig verwendet Exchange beginnend mit Exchange 2007 SP1-Versionen selbstsignierten X509 Zertifikate, um Anrufe von EWS zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="e7efe-105">By default, versions of Exchange starting with Exchange 2007 SP1 use self-signed X509 certificates to authenticate calls from EWS.</span></span> <span data-ttu-id="e7efe-106">Wenn Sie die EWS Managed API verwenden, müssen Sie eine Rückrufmethode des Zertifikat-Validierung erstellen. Andernfalls werden EWS Managed API Anforderungen fehl.</span><span class="sxs-lookup"><span data-stu-id="e7efe-106">When you are using the EWS Managed API, you need to create a certificate validation callback method; otherwise, EWS Managed API requests will fail.</span></span> <span data-ttu-id="e7efe-107">Wenn Sie den AutoErmittlungsdienst verwenden, wird der Anruf an die EWS Managed API AutoErmittlung-Methode ein **AutodiscoverLocalException** Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="e7efe-107">If you are using the Autodiscover service, the call to the EWS Managed API Autodiscover method will fail with an **AutodiscoverLocalException** error.</span></span> <span data-ttu-id="e7efe-108">Wenn Sie einen Web generierte Webdienstproxy verwenden, Sie auch möglicherweise erstellen eine Rückrufmethode Validierung abhängig davon, wie der Proxy erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e7efe-108">If you are using a web-generated web service proxy, you might also have to create a validation callback method, depending on how the proxy is created.</span></span> 
  
## <a name="prerequisites-for-creating-a-validation-callback-method"></a><span data-ttu-id="e7efe-109">Voraussetzungen für das Erstellen einer Rückrufmethode Validierung</span><span class="sxs-lookup"><span data-stu-id="e7efe-109">Prerequisites for creating a validation callback method</span></span>
<span data-ttu-id="e7efe-110"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="e7efe-110"></span></span>

<span data-ttu-id="e7efe-111">Zum Einrichten ein Serverzertifikats überprüfen, stellen Sie sicher, dass Folgendes zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e7efe-111">To set up to validate a server certificate, ensure that the following are true:</span></span> 
  
- <span data-ttu-id="e7efe-112">Der Exchange-Server ist ein selbstsigniertes Zertifikat für EWS geeignet.</span><span class="sxs-lookup"><span data-stu-id="e7efe-112">Your Exchange server is using a self-signed certificate for EWS.</span></span> <span data-ttu-id="e7efe-113">Wenn der Administrator ein gültiges Zertifikat, das aufzeichnet, ein Stammzertifikat installiert hat, müssen Sie keine Rückrufmethode Validierung erstellen.</span><span class="sxs-lookup"><span data-stu-id="e7efe-113">If the administrator has installed a valid certificate that traces to a root certificate, you do not need to create a validation callback method.</span></span> 
    
- <span data-ttu-id="e7efe-114">Sie erstellen eine verwaltete Anwendung, die einen Verweis auf die folgenden erforderlichen .NET Framework-Namespaces enthält:</span><span class="sxs-lookup"><span data-stu-id="e7efe-114">You are creating a managed application that includes a reference to the following required .NET Framework namespaces:</span></span> 
    
  - <span data-ttu-id="e7efe-115">**System.Net**</span><span class="sxs-lookup"><span data-stu-id="e7efe-115">**System.Net**</span></span>
  - <span data-ttu-id="e7efe-116">**System.Net.Security**</span><span class="sxs-lookup"><span data-stu-id="e7efe-116">**System.Net.Security**</span></span>  
  - <span data-ttu-id="e7efe-117">**System.Security.Cryptography.X509Certificates**</span><span class="sxs-lookup"><span data-stu-id="e7efe-117">**System.Security.Cryptography.X509Certificates**</span></span>
    
## <a name="example-callback-method-to-validate-a-server-certificate-for-the-ews-managed-api"></a><span data-ttu-id="e7efe-118">Beispiel: Rückrufmethode zum Überprüfen eines Serverzertifikats für die EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="e7efe-118">Example: Callback method to validate a server certificate for the EWS Managed API</span></span>
<span data-ttu-id="e7efe-119"><a name="bk_example"> </a></span><span class="sxs-lookup"><span data-stu-id="e7efe-119"></span></span>

<span data-ttu-id="e7efe-120">Im folgenden Codebeispiel wird veranschaulicht, wie ein X509 erstellen Validierung Rückrufmethode für die EWS Managed API-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="e7efe-120">The following code example shows how to create an X509 certificate validation callback method for the EWS Managed API.</span></span> <span data-ttu-id="e7efe-121">Diese Methode wird ein X509 überprüfen Zertifikat und nur true zurück, wenn eine der folgenden Kriterien erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="e7efe-121">This method will validate an X509 certificate and only return true when either of the following criteria are met:</span></span> 
  
- <span data-ttu-id="e7efe-122">Das Zertifikat ist gültig und wieder zu einem gültigen Stammzertifikat verfolgt.</span><span class="sxs-lookup"><span data-stu-id="e7efe-122">The certificate is valid and traces back to a valid root certificate.</span></span>    
- <span data-ttu-id="e7efe-123">Das Zertifikat ist gültig und selbstsigniert vom Server, der es zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e7efe-123">The certificate is valid and is self-signed by the server that returned it.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="e7efe-124">Die Zertifikat Überprüfung Rückrufmethode in diesem Beispiel bietet ausreichend Sicherheit für entwickeln und Testen von EWS Managed API-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="e7efe-124">The certificate validation callback method in this example provides sufficient security for development and testing of EWS Managed API applications.</span></span> <span data-ttu-id="e7efe-125">Jedoch könnte es bietet keine ausreichende Sicherheit für die Anwendung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e7efe-125">However, it might not provide sufficient security for your deployed application.</span></span> <span data-ttu-id="e7efe-126">Sie sollten sicherstellen, dass die Rückrufmethode Zertifikat Überprüfung, mit denen Sie die Sicherheit Ihrer Organisation erfüllt.</span><span class="sxs-lookup"><span data-stu-id="e7efe-126">You should always make sure that the certificate validation callback method that you use meets the security requirements of your organization.</span></span> 
  
```cs
      private static bool CertificateValidationCallBack(
         object sender,
         System.Security.Cryptography.X509Certificates.X509Certificate certificate,
         System.Security.Cryptography.X509Certificates.X509Chain chain,
         System.Net.Security.SslPolicyErrors sslPolicyErrors)
    {
      // If the certificate is a valid, signed certificate, return true.
      if (sslPolicyErrors == System.Net.Security.SslPolicyErrors.None)
      {
        return true;
      }
      // If there are errors in the certificate chain, look at each error to determine the cause.
      if ((sslPolicyErrors &amp; System.Net.Security.SslPolicyErrors.RemoteCertificateChainErrors) != 0)
      {
        if (chain != null &amp;&amp; chain.ChainStatus != null)
        {
          foreach (System.Security.Cryptography.X509Certificates.X509ChainStatus status in chain.ChainStatus)
          {
            if ((certificate.Subject == certificate.Issuer) &amp;&amp;
               (status.Status == System.Security.Cryptography.X509Certificates.X509ChainStatusFlags.UntrustedRoot))
            {
              // Self-signed certificates with an untrusted root are valid. 
              continue;
            }
            else
            {
              if (status.Status != System.Security.Cryptography.X509Certificates.X509ChainStatusFlags.NoError)
              {
                // If there are any other errors in the certificate chain, the certificate is invalid,
             // so the method returns false.
                return false;
              }
            }
          }
        }
        // When processing reaches this line, the only errors in the certificate chain are 
    // untrusted root errors for self-signed certificates. These certificates are valid
    // for default Exchange server installations, so return true.
        return true;
      }
      else
      {
     // In all other cases, return false.
        return false;
      }
    }

```

<span data-ttu-id="e7efe-127">Verwenden Sie die **ServicePointManager** -Klasse in .NET **System.Net** -Namespace, verknüpfen Sie eine Rückrufmethode Überprüfung durch Festlegen der **ServerCertificateValidationCallback** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e7efe-127">You use the **ServicePointManager** class in the .NET **System.Net** namespace to hook up a validation callback method by setting the **ServerCertificateValidationCallback** property.</span></span> <span data-ttu-id="e7efe-128">Ähnlichen Code wie im folgenden Codebeispiel können Sie die **ServerCertificateValidationCallback** -Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e7efe-128">You can use code similar to the following code example to set the **ServerCertificateValidationCallback** property.</span></span> 
  
```cs
ServicePointManager.ServerCertificateValidationCallback = CertificateValidationCallBack;

```

## <a name="next-steps"></a><span data-ttu-id="e7efe-129">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="e7efe-129">Next steps</span></span>
<span data-ttu-id="e7efe-130"><a name="bk_example"> </a></span><span class="sxs-lookup"><span data-stu-id="e7efe-130"></span></span>

<span data-ttu-id="e7efe-131">Nachdem Sie die Validation-Rückrufmethode für die EWS Managed API erstellt haben, können Sie den AutoErmittlungsdienst verwenden, Verbindungspunkte sowie Benutzer- und domäneneinstellungen aus einem Exchange-Server abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e7efe-131">After you have created the validation callback method for the EWS Managed API, you can use the Autodiscover service to get connection points and user and domain settings from an Exchange server.</span></span> <span data-ttu-id="e7efe-132">Weitere Informationen finden Sie unter den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="e7efe-132">For more information, see the following articles:</span></span>
  
- [<span data-ttu-id="e7efe-133">Mithilfe von AutoErmittlung Verbindungspunkte suchen</span><span class="sxs-lookup"><span data-stu-id="e7efe-133">Use Autodiscover to find connection points</span></span>](how-to-use-autodiscover-to-find-connection-points.md)
    
- [<span data-ttu-id="e7efe-134">Abrufen von benutzereinstellungen aus Exchange mithilfe der AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="e7efe-134">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [<span data-ttu-id="e7efe-135">Abrufen von domäneneinstellungen aus einem Exchange-server</span><span class="sxs-lookup"><span data-stu-id="e7efe-135">Get domain settings from an Exchange server</span></span>](how-to-get-domain-settings-from-an-exchange-server.md)
    
## <a name="see-also"></a><span data-ttu-id="e7efe-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7efe-136">See also</span></span>

- [<span data-ttu-id="e7efe-137">Einrichten Ihrer EWS-Anwendung</span><span class="sxs-lookup"><span data-stu-id="e7efe-137">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)  
- [<span data-ttu-id="e7efe-138">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="e7efe-138">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    

