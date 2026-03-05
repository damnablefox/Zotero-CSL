| {{ itemType }}             | **条目类型**          | `Item Type`                | 父条目类型。条目的广义类型。条目类型通常根据条目应如何被引用来确定。请参阅上文对 Zotero 条目类型的描述。您可以在类型(`Type`)、格式(`Format`)或其他(`Extra`)字段中，或使用 [标签]，来存储关于条目类型的更具体信息（例如，是小说还是传记类图书）。 |
| {{ title }}                | **标题**              | `Title`                    | 父条目的标题。应以句首字母大写的方式输入。`Case Name` 司法案例父条目标题；`subject` 电子邮件父条目条目标题；`Name Of Act` 法律父条目标题。 |
| {{ shortTitle }}           | **短标题**            | `Short Title`              | 标题的简短形式，通常不带副标题。主要用于脚注风格中的后续引用。 |
| {{ attachmentTitle }}      | 全条目支持            | `attachmentTitle`          | 正在被重命名或创建的附件的标题。 |
| {{ creators }}             | **创建者**            | `Creators`                 | 父条目的所有创作者，与作品相关的个人或实体。一个条目可以有多个不同类型的创建者。请参阅下面的创建者类型列表。 |
| {{ creatorsCount }}        | 全条目支持            | `creatorsCount`            | 父条目所有创作者的总数。（Zotero 7.0.16） |
| {{ firstCreator }}         | 全条目支持            | `firstCreator`             | 父条目的创作者（1-2 位作者或编辑），与主面板中的“创作者”列的值相同。 |
| {{ authors }}              | 全条目支持            | `authors`                  | 父条目的主要创作者（取决于条目类型(`Item Type`)，这些是作者或艺术家，但不包括编辑或其他贡献者）。 |
| {{ authorsCount }}         | 全条目支持            | `authorsCount`             | 父条目主要创作者的数量。（Zotero 7.0.16） |
| {{ editors }}              |                       | `editors` `Series Editors` | 父条目的编辑(`editors`)和丛书编辑(`Series Editors`)字段。图书编辑丛书编辑、图书章节编辑丛书编辑、会议论文编辑丛书编辑、词条编辑丛书编辑、百科条目编辑丛书编辑、报告编辑丛书编辑、文档编辑、期刊文章编辑、标准编辑、预印本编辑、地图丛书编辑。 |
| {{ editorsCount }}         |                       | `editorsCount`             | 父条目编辑和丛书编辑的数量。（Zotero 7.0.16） |
| {{ abstractNote }}         | **摘要**              | `Abstract`                 | 作品的简短描述。 |
| {{ date }}                 | **日期**              | `Date`                     | 出版日期。对于电子资源的访问日期，使用“访问日期(`Accessed`)”。 |
| {{ year }}                 | 全条目支持            | `year`                     | 年份，从父条目的日期(`Date`)字段中提取。 |
| {{ language }}             | **语言**              | `Language`                 | 条目的出版语言。软件使用编程语言(`Prog.Language`)。我们建议将其存储为两个字母的[ISO语言代码]，后跟两个字母的[ISO国家/地区代码]（例如，en-US 表示美式英语，de-DE 表示德语）。**语言**字段用于确定在格式化条目标题时是否应应用[英文标题大小写规则]。如果存储的条目数据是英文的（例如，对于翻译后的标题），即使条目内容是另一种语言，也应输入 en-US 或 en-UK。 |
| {{ programmingLanguage }}  | 软件条目              | `Prog.Language`            | 软件编程语言。 |
| {{ citationKey }}          | 全条目支持            | `Citation Key`             | 引用关键词字段。 |
| {{ publicationTitle }}     | **出版物**            | `Publication`              | 包含被引用条目的期刊（期刊、杂志、报纸等）的标题。包括以下字段：`Publication` 期刊文章出版物、杂志文章出版物、报纸文章出版物；`Book Title` 图书章节书名；`Blog Title` 博客标题；`Proceedings Title` 会议论文集标题；`Dictionary Title` 词条词典标题；`Encyclopedia Title` 百科条目百科标题；`Forum/Listserv Title` 论坛帖子论坛/列表服务标题；`Session Title` 演示文档分会场标题；`Program Title` 电视广播节目名称、电台广播节目名称。 |
| {{ bookTitle }}            | **书名**              | `Book Title`               | 章节、词条或其他图书部分所在的图书、百科全书或词典的标题。 |
| {{ encyclopediaTitle }}    | **百科标题**          | `Encyclopedia Title`       | 章节、词条或其他图书部分所在的图书、百科全书或词典的标题。 |
| {{ dictionaryTitle }}      | **词典标题**          | `Dictionary Title`         | 章节、词条或其他图书部分所在的图书、百科全书或词典的标题。 |
| {{ volume }}               | **卷次**              | `Volume`                   | 文章或章节所在的（通常是多卷）出版物的卷号。对于数字卷号，仅输入数字。如果引用时需要同时包含卷标题，请在此字段中包含标题（例如，“2：组织心理学”）。包括以下字段：`Volume` 音频卷次、图书卷次、图书章节卷次、会议论文卷次、词条卷次、百科条目卷次、期刊文章卷次、杂志文章卷次、报纸文章卷次、视频卷次；`Code Volume` 法案法典卷次；`Reporter Volume` 司法案例报告系统卷次。 |
| {{ issue }}                | **期号**              | `Issue`                    | 期刊的期号。通常，每期在每年/每卷开始时从 1 开始编号。如果期刊只有卷号而没有期号，请将此字段留空。`Issue` 会议论文期号、期刊文章期号、杂志文章期号、报纸文章期号。 |
| {{ pages }}                | **页码**              | `Pages`                    | 作为较大出版物一部分的条目的页码范围。也用于电子期刊和电子图书中的定位符或文章编号。包括以下字段：`Pages` 图书章节页码、会议论文页码、词条页码、百科条目页码、听证会页码、期刊文章页码、杂志文章页码、报纸文章页码、专利页码、报告页码、法律页码；`Code Pages` 法案法典页码；`First Page` 司法案例起始页。 |
| {{ edition }}              | **版本**              | `Edition`                  | 作品的版本。如果是数字，请简化为阿拉伯数字（即，输入“2”而不是“second”）。`Edition` 图书版本、图书章节版本、词条版本、百科条目版本、地图版本、报纸文章版本、标准版本。 |
| {{ series }}               | **系列**              | `Series`                   | 包含多个出版物或演示文稿的丛书名称（例如，“剑桥比较政治学研究”，“人格评估进展特刊”）。`Series` 图书系列、图书章节系列、会议论文系列、词条系列、百科条目系列、期刊文章系列、演示文档系列、学位论文系列、预印本系列。 |
| {{ seriesNumber }}         | **系列编号**          | `Series Number`            | 条目在丛书中的编号。`Series Number` 图书系列编号、图书章节系列编号、会议论文系列编号、词条系列编号、百科条目系列编号、报告系列编号、学位论文系列编号、预印本系列编号。 |
| {{ seriesTitle }}          | **系列标题**          | `Series Title`             | 期刊一期中一系列文章的标题（例如，一个专题部分或“封面故事”）。将其称为“部分标题”可能更合适。有关说明，请参见[此处][系列标题]。出于引用目的，此字段目前等同于“丛书(`Series`)”，并且在某些条目类型（例如，音频(`Audio Recording`)、地图(`Map`)条目。）中被错误地用作丛书。`Series Title` 音频系列标题、期刊文章系列标题、地图系列标题、播客系列标题、报告系列标题、软件系列标题、视频系列标题。 |
| {{ numberOfVolumes }}      | **总卷数**            | `# of Volumes`             | 集体作品的总卷数。`# of Volumes` 音频总卷数、图书总卷数、图书章节总卷数、会议论文总卷数、词条总卷数、百科条目总卷数、听证会总卷数、视频总卷数。 |
| {{ numPages }}             | **总页数**            | `# of Pages`               | 图书的总页数。`# of Pages` 图书总页数、手稿总页数、标准总页数、学位论文总页数。 |
| {{ section }}              | **条文序号**          | `Section`                  | 报纸的版次或部分。`Section` 法案条文序号、期刊文章条文序号、报纸文章条文序号、法律条文序号。 |
| {{ place }}                | **地点**              | `Place`                    | 条目的出版地点。包括以下字段：`Place` 音频地点、图书地点、图书章节地点、会议论文地点、词条地点、文档地点、百科条目地点、电影地点、听证会地点、采访稿地点、期刊文章地点、杂志文章地点、手稿地点、地图地点、报纸文章地点、专利地点、播客地点、演示文档地点、电台广播地点、报告地点、软件地点、标准地点、学位论文地点、电视广播地点、视频地点、预印本地点；`Repo. Location` 数据集仓库位置。 |
| {{ publisher }}            | **出版社**            | `Publisher`                | 条目的出版者。包括以下字段：`Publisher` 图书出版社、图书章节出版社、会议论文出版社、词条出版社、文档出版社、百科条目出版社、听证会出版社、采访稿出版社、期刊文章出版社、杂志文章出版社、地图出版社、报纸文章出版社、播客出版社、标准出版社；`Label` 音频标记；`Repository` 数据集仓库、预印本仓库；`Distributor` 电影分发者；`Institution` 手稿机构组织、报告机构组织；`Network` 电台广播网络、电视广播网络；`Company`软件公司；`University` 学位论文大学；`Studio` 视频工作室。 |
| {{ journalAbbreviation }}  | **刊名简称**          | `Journal Abbr`             | 期刊的缩写标题。使用 Zotero Word 或 LibreOffice 插件时，Zotero 可以使用 MEDLINE 列表自动缩写标题。使用此字段输入基于其他系统的缩写，或在文字处理器之外生成参考文献目录。 |
| {{ ISBN }}                 | **ISBN**              | `ISBN`                     | 图书或其他出版物的[国际标准书号]。`ISBN` 图书、图书章节、会议论文、报告、学位论文、标准、软件、地图、音频、视频、词条、百科条目。 |
| {{ ISSN }}                 | **ISSN**              | `ISSN`                     | 期刊或连续出版物的[国际标准连续出版物号]。`ISSN` 图书、图书章节、会议论文、报告、学位论文、期刊文章、杂志文章、报纸文章、博客帖子。 |
| {{ sessionTitle }}         | 演示文档条目          | `Session Title`            | 演示文档分会场标题。 |
| {{ repositoryLocation }}   | 数据集条目            | `Repo. Location`           | 数据集仓库位置。 |
| {{ repository }}           | 仓库                  | `Repository`               | 数据集仓库、预印本仓库。 |
| {{ seriesText }}           | 期刊文章条目          | `Series Text`              | 期刊文章系列描述。 |
| {{ accessDate }}           | **访问日期**          | `Accessed`                 | UTC 格式的访问日期，如果存在 `timeZone` 参数，则转换为指定的时区。（Zotero 8）访问电子资源的日期。通常自动填写。您可以输入“today”、“yesterday”和“tomorrow”以快速输入相应日期。 |
| {{ DOI }}                  | **DOI**               | `DOI`                      | 条目的[数字对象标识符]。对于期刊文章以外的条目，DOI 可以存储在其他(`Extra`)字段中。请参阅下面的从其他(`Extra`)字段引用。 |
| {{ url }}                  | **URL**               | `URL`                      | 访问完整条目的网址。不要使用此字段链接到目录记录（例如，图书馆或 Google Books）或摘要——这些应作为链接添加。 |
| {{ archive }}              | **档案**              | `Archive`                  | 主要用于档案资源，指发现条目的档案馆。也用于存储库，例如政府报告数据库、机构知识库或学科知识库。`Archive` 艺术品档案、音频档案、图书档案、图书章节档案、会议论文档案、数据集档案、词条档案、文档档案、百科条目档案、电影档案、采访稿档案、期刊文章档案、信件档案、杂志文章档案、手稿档案、地图档案、报纸文章档案、电台广播档案、报告档案、软件档案、标准档案、学位论文档案、电视广播档案、视频档案、预印本档案。 |
| {{ archiveLocation }}      | **存档位置**          | `Loc. in Archive`          | 条目在档案馆中的位置，例如盒号和文件夹号，或查找工具中的其他相关位置信息。将子收藏/索书号、盒号和文件夹号一起包含在此字段中。有关在 Zotero 中引用档案资料的更多提示，请参见[此处][存档位置]。`Loc. in Archive` 艺术品存档位置、音频存档位置、图书存档位置、图书章节存档位置、会议论文存档位置、数据集存档位置、词条存档位置、文档存档位置、百科条目存档位置、电影存档位置、采访稿存档位置、期刊文章存档位置、信件存档位置、杂志文章存档位置、手稿存档位置、地图存档位置、报纸文章存档位置、电台广播存档位置、报告存档位置、软件存档位置、标准存档位置、学位论文存档位置、电视广播存档位置、视频存档位置、预印本存档位置。 |
| {{ libraryCatalog }}       | **文库编目**          | `Library Catalog`          | 导入条目的目录或数据库。例如，在 MLA 引用风格中使用此字段。此字段的用途比实际的图书馆目录更广泛。`Library Catalog` 艺术品文库编目、音频文库编目、图书文库编目、图书章节文库编目、会议论文文库编目、数据集文库编目、词条文库编目、文档文库编目、百科条目文库编目、电影文库编目、采访稿文库编目、期刊文章文库编目、信件文库编目、杂志文章文库编目、手稿文库编目、地图文库编目、报纸文章文库编目、电台广播文库编目、报告文库编目、软件文库编目、标准文库编目、学位论文文库编目、电视广播文库编目、视频文库编目、预印本文库编目。 |
| {{ callNumber }}           | **索书号**            | `Call Number`              | 条目在图书馆中的索书号。对于引用档案资料，如果适用，也请将索书号包含在**档案馆位置**中。`Call Number` 艺术品索书号、音频索书号、图书索书号、图书章节索书号、会议论文索书号、数据集索书号、词条索书号、文档索书号、百科条目索书号、电影索书号、采访稿索书号、期刊文章索书号、信件索书号、杂志文章索书号、手稿索书号、地图索书号、报纸文章索书号、电台广播索书号、报告索书号、软件索书号、标准索书号、学位论文索书号、电视广播索书号、视频索书号、预印本索书号。 |
| {{ type }}                 | **类型**              | `Type`                     | 报告的类型（例如，“技术报告”、“CPTO 技术简报”）或学位论文的类型（例如，“博士学位论文”、“博士论文”、“硕士论文”；如适用，应包含“thesis”或“dissertation”字样）。地图类型，信件类型，论文类型，手稿类型，演稿类型，标准类型，文档类型，数据集类型；`Genre` 电影分类，预印本分类；`Post Type` 论坛帖子类型；`Report Type` 报告类型；`Website Type` 博客帖子网站类型；`File Type` 播客音频文件类型。 |
| {{ reportType }}           | **报告类型**          | `Report Type`              | 报告的类型（例如，“技术报告”、“CPTO 技术简报”）。 |
| {{ reportNumber }}         | **报告编号**          | `Report Number`            | 报告的编号。不要包含“Number”、“No.”、“Nº”、“№”等字样或类似内容；引用样式会自动添加这些内容。 |
| {{ institution }}          | **机构组织**          | `Institution`              | 发布报告的研究机构。发布手稿的机构组织。 |
| {{ university }}           | **大学**              | `University`               | 授予学位论文学位的大学。 |
| {{ thesisType }}           | 论文条目              | `Type`                     | 论文类型。 |
| {{ letterType }}           | 信件条目              | `Type`                     | 信件类型。 |
| {{ manuscriptType }}       | 手稿条目              | `Type`                     | 手稿类型。 |
| {{ presentationType }}     | 演示文档条目          | `Type`                     | 演稿类型。 |
| {{ proceedingsTitle }}     | **论文集标题**        | `Proceedings Title`        | 发表会议论文的会议论文集标题。 |
| {{ conferenceName }}       | **会议名称**          | `Conference Name`          | 发表会议论文的会议名称。 |
| {{ meetingName }}          | **演示会议名称**      | `Meeting Name`             | 进行演示的会议名称。 |
| {{ place }}                | **地点**              | `Place`                    | 对于**演示文稿**，指举行会议或进行演示的地点。对于**会议论文**（发表在会议论文集中），使用此字段表示论文集的出版地点。如果需要同时提供出版地点和会议地点的不同位置，请将此字段留空，并将事件地点(`Event Place`)和出版地点(`Publisher Place`)字段添加到其他(`Extra`)字段中（请参阅下面的从其他字段引用）。`Place` 音频地点、图书地点、图书章节地点、会议论文地点、词条地点、文档地点、百科条目地点、电影地点、听证会地点、采访稿地点、期刊文章地点、杂志文章地点、手稿地点、地图地点、报纸文章地点、专利地点、播客地点、演示文档地点、电台广播地点、报告地点、软件地点、标准地点、学位论文地点、电视广播地点、视频地点、预印本地点；`Repo. Location` 数据集仓库位置。 |
| {{ type }}                 | **类型**              | `Type`                     | 演示的类型或格式（例如，“海报”、“研讨会”、“特邀报告”）。`Type` 地图类型，信件类型，论文类型，手稿类型，演稿类型，标准类型，文档类型，数据集类型；`Genre` 电影分类，预印本分类；`Post Type` 论坛帖子类型；`Report Type` 报告类型；`Website Type` 博客帖子网站类型；`File Type` 播客音频文件类型。 |
| {{ format }}               | **格式**              | `Format`                   | 图书、数据集、音频或视频录制的格式。音频和视频格式使用 `audioRecordingFormat` 和 `videoRecordingFormat` 变量。 |
| {{ videoRecordingFormat }} | 视频格式              | `Format`                   | 视频格式、电视广播视频格式、电影视频格式。 |
| {{ audioRecordingFormat }} | 音频格式              | `Format`                   | 音频格式、电台广播音频格式。 |
| {{ audioFileType }}        | **文件类型**          | `File Type`                | 音频或视频录制的格式（例如“DVD”、“CD”、“MP3”等）。 |
| {{ runningTime }}          | **时长**              | `Running Time`             | 任何类型录制的总时长。输入时带单位（例如 120 分钟）。`Running Time` 音频时长、电影时长、播客时长、电台广播时长、电视广播时长、视频时长。 |
| {{ programTitle }}         | **节目名称**          | `Program Title`            | 某一集节目所属的广播或电视节目的标题（例如，“美国生活”或“60 分钟”）。`Program Title` 电视广播节目名称、电台广播节目名称。 |
| {{ episodeNumber }}        | **集数**              | `Episode Number`           | 播客或电视/广播广播的集号。`Episode Number` 播客集数、电台广播集数、电视广播集数。 |
| {{ network }}              | **网络**              | `Network`                  | 播放电视或广播节目的网络或电视台。 |
| {{ label }}                | **音频标记**          | `Label`                    | 在市场上发行音频录制的唱片公司。 |
| {{ distributor }}          | **分发者**            | `Distributor`              | 在市场上发行电影的组织。 |
| {{ studio }}               | **工作室**            | `Studio`                   | 制作视频录制的制片厂。 |
| {{ genre }}                | **分类**              | `Genre`                    | 电影的类型（例如，“恐怖片”）。 |
| {{ artworkMedium }}        | **媒介**              | `Medium`                   | 艺术品或图表的类型，或其创作所用的媒介（例如，“水彩画”、“木雕”、“X 射线晶体图”、“散点图”）。 |
| {{ artworkSize }}          | **艺术品尺寸**        | `Artwork Size`             | 艺术品或图表的尺寸。 |
| {{ scale }}                | **比例尺**            | `Scale`                    | 地图或模型的比例尺。 |
| {{ mapType }}              | **类型**              | `Type`                     | 对于地图，指地图的具体类型或类别的描述。 |
| {{ type }}                 | **类型**              | `Type`                     | 报告的类型（例如，“技术报告”、“CPTO 技术简报”）或学位论文的类型（例如，“博士学位论文”、“博士论文”、“硕士论文”；如适用，应包含“thesis”或“dissertation”字样）。地图类型，信件类型，论文类型，手稿类型，演稿类型，标准类型，文档类型，数据集类型；`Genre` 电影分类，预印本分类；`Post Type` 论坛帖子类型；`Report Type` 报告类型；`Website Type` 博客帖子网站类型；`File Type` 播客音频文件类型。 |
| {{ interviewMedium }}      | **媒介**              | `Medium`                   | 对于访谈，指访谈记录的格式（例如，“音频录制”、“视频录制”、“文字稿”）。 |
| {{ type }}                 | **类型**              | `Type`                     | 对于信件，指信件具体类型或用途的描述（例如，“私人通信”）。对于手稿，指手稿类型或状态的描述（例如，“未发表手稿”、“已提交出版的手稿”、“工作论文”）。 |
| {{ letterType }}           | 信件条目              | `Type`                     | 信件类型。 |
| {{ manuscriptType }}       | 手稿条目              | `Type`                     | 手稿类型。 |
| {{ thesisType }}           | 论文条目              | `Type`                     | 论文类型。 |
| {{ type }}                 | **类型**              | `Type`                     | 地图类型，信件类型，论文类型，手稿类型，演稿类型，标准类型，文档类型，数据集类型；`Genre` 电影分类，预印本分类；`Post Type` 论坛帖子类型；`Report Type` 报告类型；`Website Type` 博客帖子网站类型；`File Type` 播客音频文件类型。 |
| {{ presentationType }}     | 演示文档条目          | `Type`                     | 演稿类型。 |
| {{ subject }}              | **主题**              | `Subject`                  | 电子邮件的主题。 |
| {{ websiteTitle }}         | **网站标题**          | `Website Title`            | 包含帖子或特定网页的博客或网站标题。`{{ websiteTitle }}` 变量似乎被废弃了。 |
| {{ blogTitle }}            | **博客标题**          | `Blog Title`               | 包含帖子或特定网页的博客或网站标题。 |
| {{ forumTitle }}           | **论坛/列表服务标题** | `Forum/Listserv Title`     | 发表帖子的论坛或列表服务名称。 |
| {{ websiteType }}          | **网站类型**          | `Website Type`             | 很少使用。描述网页的类型，例如“个人博客”或“内联网”。 |
| {{ postType }}             | **帖子类型**          | `Post Type`                | 论坛帖子具体类型的描述（例如，“推文”或“Facebook 评论”）。 |
| {{ versionNumber }}        | **版本**              | `version`                  | 计算机程序的版本。`version` 数据集版本、软件版本、标准版本。 |
| {{ system }}               | **系统**              | `System`                   | 计算机程序所针对的操作系统或平台。 |
| {{ company }}              | **公司**              | `Company`                  | 发布计算机程序的组织。 |
| {{ programmingLanguage }}  | **语言**              | `Prog.Language`            | 编写计算机程序所用的编程语言。请注意，**计算机程序**对**语言**字段的使用方式与其他项目不同。 |
| {{ rights }}               | **版权\***            | `License`                  | 条目的版权条款、许可或发布状态。 |
| {{ extra }}                | **其他**              | `Extra`                    | 用于存储附加信息的自由字段。您还可以存储未包含在条目字段中的附加变量，这些变量可用于制作引文和参考文献目录。请参阅下面的从**额外**字段引用。 |
| 变量未知                   | **添加日期**          | `Date Added`               | 条目在 Zotero 中添加的日期和时间。此字段自动填写。 |
| 变量未知                   | **修改日期**          | `Date Modified`            | 条目在 Zotero 中最后修改的日期和时间。此字段自动填写并更新。 |
| {{ nameOfAct }}            | **法律名称**          | `Name Of Act`              | 法律的全称。 |
| {{ billNumber }}           | **法案编号**          | `Bill Number`              | 分配给拟议立法的识别号。 |
| {{ code }}                 | **法典**              | `Code`                     | 公布法案或法规的法典名称。 |
| {{ codeVolume }}           | **法典卷次**          | `Code Volume`              | 包含法案或法规的法典卷号。 |
| {{ codeNumber }}           | **法典编号**          | `Code Number`              | 分配给立法在其出版法典中的识别号。 |
| {{ publicLawNumber }}      | **公法编号**          | `Public Law Number`        | 分配给已颁布立法的识别号。更多详情请参见此处。 |
| {{ dateEnacted }}          | **颁布日期**          | `Date Enacted`             | 法规颁布的日期。 |
| {{ section }}              | **条文序号**          | `Section`                  | 被引用的法案或法规的部分。 |
| {{ section }}              | **条文序号**          | `Section`                  | 报纸的版次或部分。`Section` 法案条文序号、期刊文章条文序号、报纸文章条文序号、法律条文序号。 |
| {{ committee }}            | **委员会**            | `Committee`                | 举行听证会的委员会。 |
| {{ documentNumber }}       | **文档编号**          | `Document Number`          | 分配给已出版的委员会听证会记录或文稿的文件识别号。 |
| {{ codePages }}            | **法典页码**          | `Code Pages`               | 包含法案或法规的法典卷中的页码。 |
| {{ legislativeBody }}      | **立法机构\***        | `Legislative Body`         | 辩论法案、举行听证会或通过立法的立法机构（议会、参议院等）。 |
| {{ session }}              | **会期**              | `Session`                  | 立法机构提出法案、通过法律或举行听证会的会期。 |
| {{ history }}              | **历史**              | `History`                  | 与法案或法律程序历史相关的资源。`History` 法案历史、司法案例历史、听证会历史、法律历史。 |
| {{ history }}              | **历史**              | `History`                  | 与法律判例程序历史相关的资源。`History` 法案历史、司法案例历史、听证会历史、法律历史。 |
| {{ caseName }}             | **司法案例名称**      | `Case Name`                | 司法案例的名称。 |
| {{ court }}                | **审判法院**          | `Court`                    | 审理法律判例的法院。 |
| {{ dateDecided }}          | **裁判时间**          | `Date Decided`             | 法律判例判决的日期。 |
| {{ docketNumber }}         | **案号**              | `Docket Number`            | 分配给待审法律判例的案卷号。 |
| {{ reporter }}             | **报告系统**          | `Reporter`                 | 公布法律判例的判例汇编名称。 |
| {{ reporterVolume }}       | **报告系统卷次**      | `Reporter Volume`          | 公布法律判例的判例汇编卷号。 |
| {{ firstPage }}            | **起始页**            | `First Page`               | 判例出现的判例汇编卷的起始页码。 |
| {{ country }}              | **国家**              | `Country`                  | 颁发专利的国家。 |
| {{ assignee }}             | **专利权人**          | `Assignee`                 | 专利所有权转让给的实体。 |
| {{ issuingAuthority }}     | **颁发机构**          | `Issuing Authority`        | 审查申请并颁发专利的机构或办事处。 |
| {{ patentNumber }}         | **专利号**            | `Patent Number`            | 分配给专利的识别号。 |
| {{ filingDate }}           | **申请日期**          | `Filing Date`              | 提交专利申请的日期。 |
| {{ issueDate }}            | **公告日期**          | `Issue Date`               | 专利正式授权的日期。 |
| {{ applicationNumber }}    | **申请号**            | `Application Number`       | 分配给专利申请的识别号。 |
| {{ priorityNumbers }}      | **优先权号**          | `Priority Numbers`         | 用于优先权要求的专利国际申请号。 |
| {{ references }}           | **参考文献**          | `References`               | 与专利历史相关的资源。 |
| {{ legalStatus }}          | **法律状态**          | `Legal Status`             | 专利或申请的法律状态。 |
| {{ number }}               | 号码                  | `Number`                   | 手稿号码、标准号码；`Bill Number` 法案编号；`Docket Number` 司法案例案号；`Identifier` 数据集识别符；`Document Number` 听证会文档编号；`Patent Number` 专利号；`Episode Number` 播客集数、电台广播集数、电视广播集数；`Report Number` 报告编号；`Public Law Number` 法律公法编号；`Archive ID` 预印本存档ID。 |
| {{ identifier }}           | 数据集条目            | `Identifier`               | 数据集识别符。 |
| {{ archiveID }}            | 预印本条目            | `Archive ID`               | 预印本存档ID。 |
| {{ status }}               | 状态                  | `Status`                   | 标准状态；`Legal Status` 专利法律状态。 |
| {{ organization }}         | 标准条目              | `Organization`             | 标准组织。 |