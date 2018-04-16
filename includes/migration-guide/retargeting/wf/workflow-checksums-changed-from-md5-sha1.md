### <a name="workflow-checksums-changed-from-md5-to-sha1"></a><span data-ttu-id="acb93-101">Изменено с MD5 на SHA1 контрольные суммы рабочего процесса</span><span class="sxs-lookup"><span data-stu-id="acb93-101">Workflow checksums changed from MD5 to SHA1</span></span>

|   |   |
|---|---|
|<span data-ttu-id="acb93-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="acb93-102">Details</span></span>|<span data-ttu-id="acb93-103">Для поддержки отладки в Visual Studio, среда выполнения рабочего процесса приводит к возникновению ошибки контрольной суммы для экземпляра рабочего процесса, используя алгоритм хэширования.</span><span class="sxs-lookup"><span data-stu-id="acb93-103">To support debugging with Visual Studio, the Workflow runtime generates a checksum for a workflow instance using a hashing algorithm.</span></span> <span data-ttu-id="acb93-104">В .NET Framework 4.6.2 и более ранних версий хэширование контрольной суммы рабочего процесса используется алгоритм MD5, вызвавшее проблемы в системах с поддержкой стандарта FIPS.</span><span class="sxs-lookup"><span data-stu-id="acb93-104">In the .NET Framework 4.6.2 and earlier versions, workflow checksum hashing used the MD5 algorithm, which caused issues on FIPS-enabled systems.</span></span> <span data-ttu-id="acb93-105">Начиная с .NET Framework 4.7, алгоритм — SHA1.</span><span class="sxs-lookup"><span data-stu-id="acb93-105">Starting with the .NET Framework 4.7, the algorithm is SHA1.</span></span> <span data-ttu-id="acb93-106">Если код имеет постоянное эти контрольные суммы, они будут несовместимы.</span><span class="sxs-lookup"><span data-stu-id="acb93-106">If your code has persisted these checksums, they will be incompatible.</span></span>|
|<span data-ttu-id="acb93-107">Предложение</span><span class="sxs-lookup"><span data-stu-id="acb93-107">Suggestion</span></span>|<span data-ttu-id="acb93-108">Если код не удалось загрузить экземпляры рабочих процессов из-за ошибки контрольной суммы, включите параметр <code>AppContext</code> переключения &quot;Switch.System.Activities.UseMD5ForWFDebugger&quot; значение true. В коде:</span><span class="sxs-lookup"><span data-stu-id="acb93-108">If your code is unable to load workflow instances due to a checksum failure, try setting the <code>AppContext</code> switch &quot;Switch.System.Activities.UseMD5ForWFDebugger&quot; to true.In code:</span></span><pre><code class="language-csharp">System.AppContext.SetSwitch(&quot;Switch.System.Activities.UseMD5ForWFDebugger&quot;, true);&#13;&#10;</code></pre><span data-ttu-id="acb93-109">Или в файле конфигурации:</span><span class="sxs-lookup"><span data-stu-id="acb93-109">Or in configuration:</span></span><pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Activities.UseMD5ForWFDebugger=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="acb93-110">Область</span><span class="sxs-lookup"><span data-stu-id="acb93-110">Scope</span></span>|<span data-ttu-id="acb93-111">Дополнительный номер</span><span class="sxs-lookup"><span data-stu-id="acb93-111">Minor</span></span>|
|<span data-ttu-id="acb93-112">Версия</span><span class="sxs-lookup"><span data-stu-id="acb93-112">Version</span></span>|<span data-ttu-id="acb93-113">4.7</span><span class="sxs-lookup"><span data-stu-id="acb93-113">4.7</span></span>|
|<span data-ttu-id="acb93-114">Тип</span><span class="sxs-lookup"><span data-stu-id="acb93-114">Type</span></span>|<span data-ttu-id="acb93-115">Изменение целевой платформы</span><span class="sxs-lookup"><span data-stu-id="acb93-115">Retargeting</span></span>|
