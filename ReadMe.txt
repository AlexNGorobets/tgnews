This project has taken a part in two Telegram DataClustering contests consequently.
Available on:
https://contest.com/docs/data_clustering
https://contest.com/docs/data_clustering2
Summary: code can take dir with html-files (articles). Each file has an agreed in advance set of fields in the header.
Program can be runned in two modes:
languages _dir_ - parse files and split articles on English and Russian (other articles dropped).
news _dir_ - does the same, but also picks only "news" articles.
Performance and words configurations given in config.xml

How do I get started?
- download the sources, 
- run src/tgclustering.cbp via Code::Blocks,
- build binary for Windows or Linux (both tested)
- unpack inputTestData.zip in folder with archive
- and run it.
Any invalid arguments show you the usage.
As the test dataset it can be used inputTest dir in the project root.
Tips:
config.xml-file should be placed in the run path - if you run a binary from console - nothing shouldn't be done.
Otherwise, if You run it from C::B - place config.xml near to the *cbp-file.

I'm a hirer, where I can look to find sth. exciting in code?
- Pretty fast simple parser with std::string_view implemented in CNode.cpp and tgparser.cpp (no double allocating of data, low cache misses etc.).
- Tricky language detector - follow std::bind() in tools.cpp.
- c++17 std::filesystem used in CFileHolder.cpp.
- Enums iterating template shown in tgtypes.h
- Multi-thread stuff in CNewsMgr::DoWork()

Have luck!