### <a name="certificate-eku-oid-validation"></a><span data-ttu-id="0b58d-101">Проверка кода Объекта EKU сертификата</span><span class="sxs-lookup"><span data-stu-id="0b58d-101">Certificate EKU OID validation</span></span>

|   |   |
|---|---|
|<span data-ttu-id="0b58d-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="0b58d-102">Details</span></span>|<span data-ttu-id="0b58d-103">Начиная с .NET Framework 4.6 <xref:System.Net.Security.SslStream> или <xref:System.Net.ServicePointManager> классы выполнять проверку идентификатор (OID) расширенного использования ключа (EKU) объекта.</span><span class="sxs-lookup"><span data-stu-id="0b58d-103">Starting with .NET Framework 4.6, the <xref:System.Net.Security.SslStream> or <xref:System.Net.ServicePointManager> classes perform enhanced key use (EKU) object identifier (OID) validation.</span></span> <span data-ttu-id="0b58d-104">Расширение расширенного использования ключа (EKU) — это коллекция идентификаторов объектов (OID), которые указывают приложения, использующие ключ.</span><span class="sxs-lookup"><span data-stu-id="0b58d-104">An enhanced key usage (EKU) extension is a collection of object identifiers (OIDs) that indicate the applications that use the key.</span></span> <span data-ttu-id="0b58d-105">Проверка Объекта EKU использует обратные вызовы удаленный сертификат, чтобы обеспечить удаленный сертификат правильно OID для своей цели.</span><span class="sxs-lookup"><span data-stu-id="0b58d-105">EKU OID validation uses remote certificate callbacks to ensure that the remote certificate has the correct OIDs for the intended purpose.</span></span>|
|<span data-ttu-id="0b58d-106">Предложение</span><span class="sxs-lookup"><span data-stu-id="0b58d-106">Suggestion</span></span>|<span data-ttu-id="0b58d-107">Если это изменение нежелательно, можно отключить проверки кода Объекта EKU сертификата путем добавления следующих переключиться на [ \<AppContextSwitchOverrides >](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) в [ \` ](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) из вашей файл конфигурации приложения:</span><span class="sxs-lookup"><span data-stu-id="0b58d-107">If this change is undesirable, you can disable certificate EKU OID validation by adding the following switch to the [\<AppContextSwitchOverrides>](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) in the [\`](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) of your app configuration file:</span></span><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Net.DontCheckCertificateEKUs=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre> <blockquote> [!IMPORTANT] <span data-ttu-id="0b58d-108">Этот параметр предоставляется для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="0b58d-108">This setting is provided for backward compatibility only.</span></span> <span data-ttu-id="0b58d-109">В противном случае его использование не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="0b58d-109">Its use is otherwise not recommended.</span></span></blockquote> |
|<span data-ttu-id="0b58d-110">Область</span><span class="sxs-lookup"><span data-stu-id="0b58d-110">Scope</span></span>|<span data-ttu-id="0b58d-111">Дополнительный номер</span><span class="sxs-lookup"><span data-stu-id="0b58d-111">Minor</span></span>|
|<span data-ttu-id="0b58d-112">Версия</span><span class="sxs-lookup"><span data-stu-id="0b58d-112">Version</span></span>|<span data-ttu-id="0b58d-113">4.6</span><span class="sxs-lookup"><span data-stu-id="0b58d-113">4.6</span></span>|
|<span data-ttu-id="0b58d-114">Тип</span><span class="sxs-lookup"><span data-stu-id="0b58d-114">Type</span></span>|<span data-ttu-id="0b58d-115">Изменение целевой платформы</span><span class="sxs-lookup"><span data-stu-id="0b58d-115">Retargeting</span></span>|
|<span data-ttu-id="0b58d-116">Затронутые API</span><span class="sxs-lookup"><span data-stu-id="0b58d-116">Affected APIs</span></span>|<ul><li><xref:System.Net.Security.SslStream?displayProperty=nameWithType></li><li><xref:System.Net.ServicePointManager?displayProperty=nameWithType></li><li><xref:System.Net.Http.HttpClient?displayProperty=nameWithType></li><li><xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType></li><li><xref:System.Net.HttpWebRequest?displayProperty=nameWithType></li><li><xref:System.Net.FtpWebRequest?displayProperty=nameWithType></li></ul>|
