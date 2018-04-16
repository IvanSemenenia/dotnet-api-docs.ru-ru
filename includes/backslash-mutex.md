<span data-ttu-id="e2353-101">Обратная косая черта (\\) является зарезервированным символом в имени мьютекса.</span><span class="sxs-lookup"><span data-stu-id="e2353-101">The backslash (\\) is a reserved character in a mutex name.</span></span> <span data-ttu-id="e2353-102">Не используйте обратную косую черту (\\) в имени мьютекс за исключением того, как указано в примечании об использовании мьютексы в сеансов сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="e2353-102">Don't use a backslash (\\) in a mutex name except as specified in the note on using mutexes in terminal server sessions.</span></span> <span data-ttu-id="e2353-103">В противном случае <xref:System.IO.DirectoryNotFoundException> может быть создано исключение, несмотря на то, что имя мьютекса представляет существующий файл.</span><span class="sxs-lookup"><span data-stu-id="e2353-103">Otherwise, a <xref:System.IO.DirectoryNotFoundException> may be thrown, even though the name of the mutex represents an existing file.</span></span>