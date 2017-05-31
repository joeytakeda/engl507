# Presentation

*Note: I use the TRC loosely in these notes (which are meant to be read aloud), sometimes meaning the report itself*

## Project Design:
> An outline of your project’s design, motivations, and content (including file types
and architecture)
* My motivation for this project is multifaceted:
  * From a pragmatic standpoint, the documents produced by the TRC are very long and are daunting to read
    * There was even a challenge built around "reading" the TRC last year, which pointed to the necessity of understanding the commissions' findings
    * What that project was foregrounding was the urgency of taking in the TRC's recommendations
    * My project doesn't want to offer the TRC as a looming challenge for settlers, which arguably subtracts from the ethos of the TRC; instead, I want to think of the TRC's findings as an important text that needs not only to be read but to be readable, accessible, and usable
  * As well, I want the TRC's reports to be democratized insofar as it need not be housed solely by the government archives or academic libraries.
  * Further, I take the decentralization of the TRC as a reminder that the TRC is a text to be studied analytically. It is an important text, of course, and one that ought to be respected in many ways, but we should also be aware of the variety of voices excluded from the TRC's narrative.
  * Again, pragmatically, it would be nice to search through the entirety of the TRC for keywords (which is difficult to do since the entire collection is thousands of pages)


* The design of the project will be a simple website, akin to Alex Gil's [Ed](https://github.com/elotroalex/ed), that will focus on readability and accessiblity
* However, I diverge from Ed's underlying principle that allows editorial complexity to sacrified for the sake of readability and ease of archiving. As I want to suggest through this project, archivability and readability are inextricably knotted with rigorously encoded and edited texts
* The documents will be produced in multiple formats: displayed in XHTML5, but available in TEI-XML and plain TXT. The corpus files will be available in TEI-XML and TXT as well, which are useful for text analysis.
* The coding underneath is still variable, but so far I think it will involve this pipeline:
  * First, taking the PDF files and using the open-source software Poppler and Tesseract to extract the underlying XML of the files (there are problems with this, however, since the text might become garbled under so many translations)
  * Then, taking the HOCR files and converting them to TEI
    * I haven't determined yet whether each book will be 1 TEI file or whether I should split it into multiple chapters
    * It will likely be chapter by chapter URLs on the site, however
  * Hand-proofing the text and structure to ensure correctness
  * Then, writing a translation from the TEI-XML to HTML5
  * Producing site from that
  * The entire site will be on GitHub, so that everything can be downloaded easily
* My proof-of-concept for this project will be one volume of the TRC: Volume 4 "Missing Children and Unmarked Burials" since it contains mostly appendices of important data. The appendix that gives the location, opening, and closing date of all residential schools will be particularly important for scholars; I am planning (in a later phase of development) to correlate those locations (using Open Maps data) to the Open Maps implemented Native Land project


> Comments on the gaps/needs your project addresses, or the intervention(s) it
makes in a particular area of scholarship

* It allows the TRC findings to be used and thought of as text (compositional)
* It gives greater flexibility of analysis and interlinking between indigenous lead projects that are concerned with the TRC (compositional) 
* Easier to read (functional)
* Archivable and much lighter weight than the PDFs (which are about 10-15mb a piece whereas the text file is at most 1.2mb) (architectural)
* It allows for the use of the wealth of resources contained within the reports (particularly statistics and bibliographies)

> Questions you have for your peers and me.

* What are the best formats for reading that you find, other than PDF (do you use Ebooks? Would it be useful to be created as that?)
* How would you interact with such a long text? Would it be useful to have saved annotations?
* Should I retain page breaks in my encoding of the text? In other words, What am I doing an edition of? Is it the book itself or just the text? Are the page breaks significant in the same way that the page breaks in a printing of Shakespeare is? It's not a semantic unit, but a stylistic unit based on the restrictions of the medium. Should I be faithful to that? (I'm leaning toward no.)
